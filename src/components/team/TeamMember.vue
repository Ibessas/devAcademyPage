<template>
  <div class="team-member">
    <img v-bind:src="getImage(image)" :alt="`Imagem de ${name}`" class="image" />

    <div class="name">{{ name }}</div>

    <div class="occupation">{{ occupation }}</div>

    <div class="social">
      <a v-if="github" :href="github" target="_blank">
        <img :src="require('@/assets/github-mark.png')" class="mark" />
      </a>
      <a v-if="linkedin" :href="linkedin" target="_blank">
        <img :src="require('@/assets/linkedin-mark.png')" class="mark" />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TeamMember',

  props: {
    image: String,
    name: String,
    occupation: String,
    linkedin: String,
    github: String
  },

  methods: {
    getImage(imageName) {
      const imagesPath = require.context('../../assets/team-member-images/');

      return imagesPath(`./${imageName}`);
    }
  }
};
</script>

<style lang="stylus">
.team-member {
  background-color: #ffffff;
  border-radius: 24px;
  box-shadow: 0 0.5em 1em -0.125em rgba(10, 10, 10, 0.1), 0 0 0 1px rgba(10, 10, 10, 0.02);
  overflow: hidden;

  .image {
    border-radius: 50%;
    margin-left: 50%;
    margin-top: 24px;
    transform: translateX(-50%);
    width: 60%;
    z-index: 1;
  }

  .name {
    color: #303030;
    font-size: 18px;
    font-weight: bold;
    letter-spacing: 2px;
    margin-top: 16px;
    text-align: center;
  }

  .occupation {
    color: #909090;
    font-size: 14px;
    font-weight: bold;
    margin-top: 4px;
    text-align: center;
  }

  .social {
    background-color: #efefef;
    display: flex;
    justify-content: center;
    margin-top: 16px;
    padding: 16px 24px;

    .mark {
      margin-left: 8px;
      width: 20px;
      z-index: 0;
    }
  }
}
</style>