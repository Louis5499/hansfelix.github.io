<template>
  <section class="selected-project" id="selected-project">
    <h3 class="section-header">Selected Projects</h3>
    <div v-for="(item, idx) in projectLists" class="section-block" :key="idx">
      <h4 class="publication-header">{{item.header}}</h4>
      <h4 class="publication-author">{{item.place}}</h4>
      <h4 class="publication-author">{{item.programming}}</h4>
      <p class="publication-paragraph">{{item.description}}</p>
      <div class="publication-link">
        <span v-if="item.links && item.links.copyright">[copyright]</span>
        <span v-if="item.links && item.links.pdf">[<a :href="item.links.pdf">pdf</a>]</span>
        <span v-if="item.links && item.links.slides">[<a :href="item.links.slides">slides></a>]</span>
        <span v-if="item.links && item.links.frontendCode">[<a :href="item.links.frontendCode">frontend-code</a>]</span>
        <span v-if="item.links && item.links.code">[<a :href="item.links.code">code</a>]</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projectLists: [
        {
          header: 'Cost-Aware Buffer Repleacement on SSD Devices',
          place: '1st prize at Final Project in Intro to Database Systems',
          programming: 'Java (Object-Oriented Programming)',
          description: 'We tried to minimize the missing rate, decrease the I/O latency and prevent redundancy by employing the algorithm with recency and frequency awareness. Also, we integrate Calvin, the Fast Distributed Transactions for Partitioned Database Systems, into our database system. It requires us to study the paper, tracing thousands of codes, figuring out how to reorganize the original transaction, communication, and buffer management system, and finally implement thousand lines of codes to fulfill the requirement. As a team leader, I mainly in charge of system design and implementation. This project was awarded the first prize in the final project competition.',
          links: {
            copyright: 'yes',
            pdf: '/files/database-pdf.pdf'
          }
        },
        {
          header: 'Remote-Controlling Robotic Arm',
          place: '3rd prize at Final Project in Intro to Embedded Systems',
          programming: 'C for MSP430 & Arduino',
          description: 'By applying the knowledge learned in the Intro. to Embedded Systems to construct the wireless robotic arm, I build cross-device communication and task scheduling mechanism, and successfully integrated the remote-controlling modules between Arduino and MSP430 and utilized servo motors to manipulate the robotic mechanism. Fortunately, the product idea was awarded the 3rd prize, and this successful experience also led me to becomes more confident in embedded system development.',
          links: {
            pdf: 'https://github.com/Louis5499/Remote-Controlling-Robotic-Arm/blob/master/Final_report_106062322.pdf',
            code: 'https://github.com/Louis5499/Remote-Controlling-Robotic-Arm'
          }
        },
        {
          header: 'Keyword Extraction and Analysis on Social Media',
          programming: 'NLP (Word Breaking, Keyword Extraction - TF-IDF), Python, Javascript(Vue.js)',
          description: `By analyzing the keywords of posts on social media (Facebook, Dcard in Taiwan), we're able to predict the public opinion toward a specific social issue. In this project, we employ the Word Breaking(CKIP-Tagger) & Keyword Extraction(TF-IDF & PF) to analyze the article, and built a website to real-time connect social media for querying.`,
          links: {
            frontendCode: 'https://github.com/Louis5499/nlp-final-web',
            code: 'https://github.com/Louis5499/nlp-final-server'
          }
        },
        {
          header: 'ML Pipeline Integration with Dragon on Kubeflow (Kubernetes)',
          programming: 'Python, Golang',
          description: `In order to build an End-to-End ML Workflow that compatible with our DRAGON(Enhanced-Dragon) scheduler, I customized the Kubeflow Component and Kubeflow Pipeline and built a End-to-End template on Kubeflow.`,
          links: {
            code: 'https://github.com/Louis5499/DRAGON-TFJob-Launcher'
          }
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
.selected-project {
  padding: 100px 0 0 0;
  .section-header {
    color: #6495b5;
    font-size: 2em;
    margin-bottom: 40px;
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
    .publication-link {
      margin: 20px 0;
    }
  }
}
</style>