<template>
  <section class="workexperience-sector" id="workexperience-sector">
    <h3 class="section-header">Work Experience</h3>
    <div v-for="(work, idx) in workExperiences" class="section-block" :key="idx">
      <a v-if="work.logoImage" :href="work.logoSrc">
        <img v-if="work.companyName === '9dynamics'" src="~/assets/icons/9d-logo.png" width="70px"/>
        <img v-if="work.companyName === 'giloo'" src="~/assets/icons/giloo-logo.png" width="70px"/>
        <img v-if="work.companyName === 'Compulsory Military Service'" src="~/assets/icons/roca.png" width="70px"/>
      </a>
      <h4 class="publication-header">{{work.companyName}}</h4>
      <h4 class="publication-author">{{work.title}}</h4>
      <h4 class="publication-author">{{work.years}}</h4>
      <p v-for="(specificItem, itemIdx) in work.implementation" class="publication-paragraph" :key="itemIdx">
        <span class="dot-in-pulication">•  </span>
        <span class="para-in-publication">{{specificItem}}</span>
      </p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      workExperiences: [
        // {
        //   companyName: 'Compulsory Military Service',
        //   logoImage: '~/assets/icons/roca.png',
        //   title: 'Riflemen',
        //   years: '2021/01 - Present',
        //   implementation: [
        //     'Fulfilling compulsory military service for 4 months as a rifleman at National Army 203 brigade'
        //   ]
        // },
        {
          companyName: '9dynamics',
          logoImage: '~/assets/icons/9d-logo.png',
          title: 'Backend Tech Leader',
          years: '2020/08 - 2020/12',
          implementation: [
            'Supervised system design (microservice), networking, database selection and integration of Social Apps',
            'Built automated DevOps mechanism such as CI/CD, monitoring on E-Commerce, Game, Social Apps projects',
            'Integrated Scrum with our DevOps process from scratch to manage well projects and coordinate team members'
          ]
        },
        {
          companyName: 'giloo',
          logoImage: '~/assets/icons/giloo-logo.png',
          logoSrc: 'https://giloo.ist/',
          title: 'System Architect & Software Developer',
          years: '2017/07 - 2020/08',
          implementation: [
            'Oversaw & led the team to reconstruct backend service from monolithic system to microservice with Kubernetes',
            'Reached 99.99 % availability by integrating auto-healing mechanism with automated monitoring system',
            'Designed and implemented real-time Multi-Provider Payment System that supports Google Pay, Apple Pay, credit card, voucher by integrating with Google, Apple and Stripe APIs and PostgreSQL & Redis Databases',
            'Implemented Role-Permission Authorization Systems supporting third-party OAuth such as Google, Apple, Facebook by using Json Web Token(JWT) and Redis Database',
            'Collaborated with KKStream & Bitmovin to develop online streaming platform with Typescript'
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.workexperience-sector {
  padding: 130px 0 0 0;
  .section-header {
    color: #6495b5;
    font-size: 2em;
    margin-bottom: 15px;
  }
  .section-block {
    margin: 50px 0;
    .publication-header {
      font-size: 1.2em;
    }
    .publication-author {
      margin: 10px 0;
      font-size: .9em;
      font-style: italic;
      font-weight: 300;
    }
    b {
      font-weight: 600;
    }
    .publication-paragraph {
      margin: 5px 0;
      display: flex;
      flex-direction: row;
      .dot-in-pulication {
        width: 10px;
        margin-right: 10px;
        display: block;
      }
      .para-in-publication {
        width: calc(100% - 10px);

      }
    }
  }
}
</style>