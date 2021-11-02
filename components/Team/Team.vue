<template>
  <div class="team">
    <div id="team" class="anchor"></div>
    <div class="team__title">
      <h3 class="team__title__main">
        Nuestro Equipo
      </h3>
      <h3 class="team__title__desc">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sapien quam quam in tempus porttitor. Malesuada et purus facilisi at facilisis id nascetur laoreet non. Ac id congue aliquet ut risus in amet ac.
      </h3>
    </div>
    <div class="team__team-members">
      <TeamMember v-for="(teamMember, index) in 3" :key="index" />
    </div>
  </div>
</template>

<script>
import TeamMember from './TeamMember.vue'
  export default {
  components: { TeamMember },
    
  }
</script>

<style lang="scss" scoped>
  .team {
    max-width: 1200px;
    width: 90%;
    margin: 0 auto;
    padding: 50px 0;
    &__title {
      text-align: center;
      margin-bottom: 30px; 
      &__main {
        padding-bottom: 20px;
        color: var(--dark-main-color);
        font-size: 26px;
        font-weight: 500;
      }
      &__desc {
        color: var(--lighter-text-color);
        font-size: 20px;
        font-weight: 300;
        line-height: 30px;
      }
    }
    &__team-members {
      display: flex;
      justify-content: space-around;
      flex-wrap: wrap;
    }
  }

  @media screen and (max-width: 800px) {
    .team {
      &__title {
        &__main {
          font-size: 22px;
        }
        &__desc {
          font-size: 18px;
        }
      }
    }
  }
</style>