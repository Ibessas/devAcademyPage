<template>
  <div class="team">
    <div style="background-color: #fff">
      <div class="team-content web-team">
        <div class="title">Time de WEB+AWS</div>

        <TeamMember
          v-for="teamMember in webTeamMembers"
          :key="teamMember.name"
          :image="teamMember.image"
          :name="teamMember.name"
          :occupation="teamMember.occupation"
          :linkedin="teamMember.linkedin"
          :github="teamMember.github"
          class="team-member"
        />
      </div>

      <div class="team-content data-science-team">
        <div class="title">Time de Ciência de Dados</div>

        <TeamMember
          v-for="teamMember in dataScienceTeamMembers"
          :key="teamMember.name"
          :image="teamMember.image"
          :name="teamMember.name"
          :occupation="teamMember.occupation"
          :linkedin="teamMember.linkedin"
          :github="teamMember.github"
          class="team-member"
        />
      </div>
    </div>
  </div>
</template>

<script>
import TeamMember from './TeamMember.vue';

export default {
  name: 'Team',

  components: {
    TeamMember
  },

  data() {
    return {
      webTeamMembers: [
        {
          image: 'caio-weliton.jpeg',
          name: 'Caio Weliton',
          occupation: 'Web Developer',
          linkedin: 'https://www.linkedin.com/in/caio-weliton/',
          github: 'https://github.com/CaioWF'
        },
        {
          image: 'diego-gaspar.jpeg',
          name: 'Diego Gaspar',
          occupation: 'Web Developer',
          linkedin: 'https://www.linkedin.com/in/diego-gaspar-259824123/',
          github: 'https://github.com/diegogasparcruz'
        },
        {
          image: 'ellyo-freitas.jpeg',
          name: 'Ellyo Freitas',
          occupation: 'Web Developer',
          linkedin: 'https://www.linkedin.com/in/ellyofreitas/',
          github: 'https://github.com/ellyofreitas'
        },
        {
          image: 'israel-bessa.jpeg',
          name: 'Israel Bessa',
          occupation: 'Web Developer',
          linkedin: 'https://www.linkedin.com/in/israel-bessa-888a40164/',
          github: 'https://github.com/Ibessas'
        },
        {
          image: 'jonas-deyvid.jpeg',
          name: 'Jonas Deyvid',
          occupation: 'Web Developer',
          linkedin: 'https://www.linkedin.com/in/jonasdeyvid/',
          github: 'https://github.com/jonasdeyvid'
        },
        {
          image: 'publio-blenilio.jpeg',
          name: 'Publio Blenilio',
          occupation: 'Web Developer',
          linkedin: 'https://br.linkedin.com/in/publio-blenilio-b97a2b130',
          github: 'https://github.com/publiosilva'
        }
      ],
      dataScienceTeamMembers: [
        {
          image: 'arthur-antunes.jpeg',
          name: 'Arthur Antunes',
          occupation: 'Data Scientist',
          linkedin: 'https://www.linkedin.com/in/arthur-antunes-a13882161/',
          github: 'https://github.com/AAntunesNDS'
        },
        {
          image: 'ian-mateus.jpeg',
          name: 'Ian Mateus',
          occupation: 'Data Scientist',
          linkedin: 'https://www.linkedin.com/in/ian-mateus-es/',
          github: 'https://github.com/ianmateusES'
        }
      ]
    };
  }
};
</script>

<style lang="stylus">
.team {
  background-color: rgba(0,0,0,0);
  float: left;
  padding: 0 5% 64px 5%;
  position relative
  .team-content {
    padding-left: 32px;
    position relative
    .title {
      color: #ffffff;
      font-size: 32px;
      font-weight: bold;
      letter-spacing: 2px;
      margin-top: 64px;
    }
    .team-member {
      float: left;
      margin-right: 32px;
      margin-top: 32px;
    }
  }
}
.web-team {
  float: left;
  width: calc(100% - 32px);
  z-index 2
  .team-member {
    width: calc(100% - 32px);
  }
}
.data-science-team {
  float: left;
  width: calc(100% - 32px);
  z-index 2
  .team-member {
    width: calc(100% - 32px);
  }
}
@media screen and (min-width: 600px) {
  .web-team {
    width: calc(100% - 32px);
    .team-member {
      width: calc(50% - 32px);
    }
  }
  .data-science-team {
    width: calc(100% - 32px);
    .team-member {
      width: calc(50% - 32px);
    }
  }
}
@media screen and (min-width: 992px) {
  .web-team {
    width: calc(100% - 32px);
    .team-member {
      width: calc(33.3% - 32px);
    }
  }
  .data-science-team {
    width: calc(100% - 32px);
    .team-member {
      width: calc(33.3% - 32px);
    }
  }
}
@media screen and (min-width: 1200px) {
  .web-team {
    width: calc(60% - 32px);
    .team-member {
      width: calc(33.3% - 32px);
    }
  }
  .data-science-team {
    width: calc(40% - 32px);
    .team-member {
      width: calc(50% - 32px);
    }
  }
}
</style>
