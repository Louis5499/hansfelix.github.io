<template>
  <section class="workexperience-sector" id="workexperience-sector">
    <h3 class="section-header">Work Experience</h3>
    <div v-for="(work, idx) in workExperiences" class="section-block" :key="idx">
      <a v-if="work.logoImage" :href="work.logoSrc">
        <img v-if="work.companyName === '9dynamics'" src="~/assets/icons/9d-logo.png" width="70px"/>
        <img v-if="work.companyName === 'giloo'" src="~/assets/icons/giloo-logo.png" width="70px"/>
      </a>
      <h4 class="publication-header">{{work.companyName}}</h4>
      <h4 class="publication-author">{{work.title}}</h4>
      <h4 class="publication-author">{{work.years}}</h4>
      <p v-for="(specificItem, itemIdx) in work.implementation" class="publication-paragraph" :key="itemIdx">{{'-  ' + specificItem}}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      workExperiences: [
        {
          companyName: '9dynamics',
          logoImage: '~/assets/icons/9d-logo.png',
          title: 'Backend Tech Leader',
          years: '2020/08 - Present',
          implementation: [
            'Supervised system design and DevOps integration of E-Commerce, Game, Social Apps projects',
            'Integrated Scrum with our DevOps process from scratch to manage well projects and coordinate team members'
          ]
        },
        {
          companyName: 'giloo',
          logoImage: '~/assets/icons/giloo-logo.png',
          logoSrc: 'https://giloo.ist/',
          title: 'System Architect & SRE',
          years: '2017/07 - 2020/08',
          implementation: [
            'Designed and Implemented Multi-Provider Payment System, Authentication Service, Real-time Streaming Service',
            'Reached 99.99 % availability by reconstructing system from monolithic system to microservice with Kubernetes'
          ]
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.workexperience-sector {
  padding: 100px 0 0 0;
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
      margin: 10px 0;
    }
  }
}
</style>