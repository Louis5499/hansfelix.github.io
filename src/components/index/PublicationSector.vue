<template>
  <section class="publication-sector" id="publication-sector">
    <h3 class="section-header">Publication</h3>
    <div class="section-block">
      <h4 class="publication-header">Deep Learning Platform on Kubernetes</h4>
      <h4 class="publication-author"><b>Min-Chi Chiang</b>, Jerry Chou</h4>
      <h4 class="publication-author">In Submission</h4>
      <p class="publication-paragraph">{{publicationParagraph}}</p>
      <div class="publication-link">
        <span>[pdf]</span>
        <span>[slides]</span>
        <span>[poster]</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      publicationParagraph: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
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