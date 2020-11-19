<template>
  <section class="workexperience-sector" id="workexperience-sector">
    <h3 class="section-header">Work Experience</h3>
    <div v-for="(work, idx) in workExperiences" class="section-block" :key="idx">
      <h4 class="publication-header">{{work.companyName}}</h4>
      <h4 class="publication-author">{{work.title}}</h4>
      <h4 class="publication-author">{{work.years}}</h4>
      <p class="publication-paragraph">{{work.implementation}}</p>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      workExperiences: [
        {
          companyName: 'giloo',
          title: 'System Architect & SRE',
          years: '2017/07 - 2020/08',
          implementation: 'Supervised 34234'
        },
        {
          companyName: '9dynamics',
          title: 'Backend Tech Leader',
          years: '2020/08 - Present',
          implementation: 'Supervised 34234'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.workexperience-sector {
  margin: 100px 0 0 0;
  .section-header {
    color: #6495b5;
    font-size: 2em;
    margin-bottom: 15px;
  }
  .section-block {
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
      margin: 20px 0;
    }
  }
}
</style>