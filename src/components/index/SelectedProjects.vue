<template>
  <section class="selected-project" id="selected-project">
    <h3 class="section-header">Selected Projects</h3>
    <h3 class="section-subheader">Companies' Projects</h3>
    <div v-for="(item, idx) in companiesList" class="section-block" :key="idx">
      <h4 class="publication-header">{{item.header}}</h4>
      <h4 class="publication-author">{{item.place}}</h4>
      <h4 class="publication-author">{{item.programming}}</h4>
      <p class="publication-paragraph">{{item.description}}</p>
      <!-- <div class="publication-link">
        <span v-if="item.links && item.links.copyright">[copyright]</span>
        <span v-if="item.links && item.links.pdf">[<a :href="item.links.pdf">pdf</a>]</span>
        <span v-if="item.links && item.links.slides">[<a :href="item.links.slides">slides></a>]</span>
        <span v-if="item.links && item.links.frontendCode">[<a :href="item.links.frontendCode">frontend-code</a>]</span>
        <span v-if="item.links && item.links.code">[<a :href="item.links.code">code</a>]</span>
      </div> -->
    </div>
    <h3 class="section-subheader" style="margin-top: 90px">Other Selected Projects</h3>
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
      companiesList: [
        {
          header: 'giloo',
          place: 'Cloud Service Orchestrating(Google Cloud Platform), System Architecting(Microservice), Full-Stack Engineering',
          programming: 'Docker, Kubernetes, Javascript(Nuxt.js / Egg.js), Typescript, Python, MySQL, Redis',
          description: 'giloo is an online-streaming platform focusing on documentaries. The streaming part is the most challenging service in this project, so we collaborate with engineers with other companies to construct a reliable streaming platform.',
        },
        {
          header: 'Map Networked Based Social App (Ongoing Startup Project)',
          place: 'Supervision, Project Leading, System Orchestrating(Microservice)',
          programming: 'Docker, Kubernetes, Golang(go-micro), Javascript(Moleculer.js), MySQL, Redis, Neo4j, MongoDB, Elasticsearch',
          description: 'Dealing with graph-based data(e.g., social network and location relation) is the most challenging part. Also, in order to construct a reliable service could overload flooding requests, we build this system based on microservice architecture, which requires us to lots of effort on fine-tuning systems and follows development constraint.',
        },
        {
          header: 'E-Commerce: MGallery',
          place: 'Backend Developing',
          programming: 'AWS, Javascript(Nuxt.js / Egg.js), MySQL, Redis',
          description: 'E-Commerce: MGallery project is an E-Commerce platform, in which we integrate Line(the most popular IM app in Taiwan) Chatbot / backend service to build a real-time payment system.',
        }
      ],
      projectLists: [
        {
          header: 'Cost-Aware Buffer Repleacement on SSD Devices',
          place: '1st prize at Final Project in Intro to Database Systems',
          programming: 'Java (Object-Oriented Programming)',
          description: 'We tried to minimize the missing rate, decrease the I/O latency and prevent redundancy by employing the algorithm with recency and frequency awareness. Also, we integrate Calvin, the Fast Distributed Transactions for Partitioned Database Systems, into our database system. It requires us to study the paper, tracing thousands of codes, figuring out how to reorganize the original transaction, communication, and buffer management system, and finally implement a thousand lines of code to fulfill the requirement. As a team leader, I mainly in charge of system design and implementation. This project was awarded the first prize in the final project competition.',
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
          header: 'Parallelize COVID-19 Infectious Simulation with CUDA and OpenMP',
          programming: 'C++, OpenMP(Multi-threading), CUDA(GPU)',
          description: 'In this project, we aim to speedup infectious simulation of the SIR Model by using parallelism skills, including OpenMP for multi-threading and GPU for CUDA programming. We proposed two solutions to efficiently accelerate the simulation process: blocked-version for multi-threading and distance-based for CUDA. Finally, we successfully speedup 6.39x with CUDA version & 2.05x with OpenMP version.',
          links: {
            pdf: 'https://github.com/Louis5499/Parallelize-COVID19-Infection-Simulation/blob/master/PP20-Final.pdf',
            code: 'https://github.com/Louis5499/Parallelize-COVID19-Infection-Simulation'
          }
        },
        {
          header: 'Keyword Extraction and Analysis on Social Media',
          programming: 'NLP (Word Breaking, Keyword Extraction - TF-IDF), Python, Javascript(Vue.js)',
          description: `By analyzing the keywords of posts on social media (Facebook, Dcard in Taiwan), we're able to predict the public opinion toward a specific social issue. In this project, we employ the Word Breaking(CKIP-Tagger) & Keyword Extraction(TF-IDF & PF) to analyze the article, and build a website to real-time connect social media for querying.`,
          links: {
            frontendCode: 'https://github.com/Louis5499/nlp-final-web',
            code: 'https://github.com/Louis5499/nlp-final-server'
          }
        },
        {
          header: 'ML Pipeline Integration with Dragon on Kubeflow (Kubernetes)',
          programming: 'Python, Golang',
          description: `In order to build an End-to-End ML Workflow that compatible with our DRAGON(Enhanced-Dragon) scheduler, I customized the Kubeflow Component and Kubeflow Pipeline and built an End-to-End template on Kubeflow.`,
          links: {
            code: 'https://github.com/Louis5499/DRAGON-TFJob-Launcher'
          }
        },
        {
          header: 'BioPro A+ Application Page',
          programming: 'Java(Backend), Javascript(Vue.js / Front-End)',
          description: `BioPro A+ is an international internship program held in NTHU and offered an exchange student program with universities in German, French, etc. During my time as the technical supervisor at Biopro organization, I'm mainly in charge of constructing an application system for intended students and the landing page of the 2020 program.`,
          links: {
            frontendCode: 'https://github.com/Louis5499/biopro',
            code: 'https://github.com/Louis5499/Biopro-Application-Server'
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
  .section-subheader {
    font-size: 1.5em;
    margin: 20px 0;
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