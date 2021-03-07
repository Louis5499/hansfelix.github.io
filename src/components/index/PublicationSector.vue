<template>
  <section class="publication-sector" id="publication-sector">
    <h3 class="section-header">Publication</h3>
    <div class="section-block">
      <h4 class="publication-header">DynamoML: Dynamic Resource Management Operators for Machine Learning Workloads</h4>
      <h4 class="publication-author"><b>Min-Chi Chiang</b> and Jerry Chou</h4>
      <h4 class="publication-author">The 11th International Conference on Cloud Computing and Services Science, CLOSER 2021</h4>
      <p class="publication-paragraph">{{publicationParagraph}}</p>
      <div class="publication-link">
        <span>[<a href="/files/CLOSER_2021_41_CR.pdf">pdf</a>]</span>
        <!-- <span>[<a href="https://drive.google.com/file/d/1_4eSeqWWbOR0P6t5G8L0g7lO5IcjW3yI/view?usp=sharing">slides</a>]</span> -->
        <!-- <span>[<a href="/files/publication_poster.pdf">poster</a>]</span> -->
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      publicationParagraph: `The recent success of deep learning applications is driven by the computing power of GPUs. However, as the workflow of deep learning becomes increasingly complicated and resource-intensive, how to manage the expensive GPU resources for Machine Learning (ML) workload becomes a critical problem. Existing resource managers mostly only focus on a single specific type of workload, like batch processing or web services, and lacks runtime optimization and application performance awareness. Therefore, this paper proposes a set of runtime dynamic management techniques (including auto-scaling, job preemption, workload-aware scheduling, and elastic GPU sharing) to handle a mixture of ML workloads consisting of modeling, training, and inference jobs. Our proposed system is implemented as a set of extended operators on Kubernetes and has the strength of complete transparency and compatibility to the application code as well as the deep learning frameworks. Our experiments conducted on AWS GPU clusters prove our approach can out-perform the native Kubernetes by 60% system throughput improvement, 70% training time reduction without causing any SLA violations on inference services.`
    }
  }
}
</script>

<style lang="scss" scoped>
.publication-sector {
  padding: 100px 0 0 0;
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