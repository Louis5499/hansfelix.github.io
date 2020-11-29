<template>
  <section class="publication-sector" id="publication-sector">
    <h3 class="section-header">Publication</h3>
    <div class="section-block">
      <h4 class="publication-header">Deep Learning Platform on Kubernetes</h4>
      <h4 class="publication-author"><b>Min-Chi Chiang</b>, Jerry Chou</h4>
      <h4 class="publication-author">In Submission</h4>
      <p class="publication-paragraph">{{publicationParagraph}}</p>
      <div class="publication-link">
        <span>[pdf(In Reviewing)]</span>
        <span>[<a href="https://drive.google.com/file/d/1_4eSeqWWbOR0P6t5G8L0g7lO5IcjW3yI/view?usp=sharing">slides</a>]</span>
        <span>[<a href="/files/publication_poster.pdf">poster</a>]</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      publicationParagraph: `Since Machine Learning and Deep Learning have become increasingly popular, these two workloads also create large computational overhead to the system. If these resource-intensive workloads haven't been coordinated well with custom scheduling policy and managing mechanism, the system would waste valuable GPU resources and increase the costs. Hence, our implementation aims to optimize deep learning workloads upon the containerized system, Kubernetes. Since the container-based system is flexible and responsive, we are targeting optimizing three typical workloads(model training, model inferencing, and model developing) in the ML Pipeline. By implementing Kubernetes Custom Operator, we apply a gang-scheduling mechanism to training jobs, making training instances elastically scale with locality awareness. Also, we consolidate notebook instance on a single GPU in order to maximize GPU utilization. Finally, we integrate KOPAS, aiming to prioritize inference pods in response to climbing clients, to guarantee SLA of inference service. We successfully reduce 2.39x total execution time and speedup  3.44x Resnet-50 model training time.`
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