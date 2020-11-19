<template>
  <section class="ted-youtube" id="ted-youtube">
    <div class="text-block">
      <img src="/images/ted-youth-logo.png" width="150px">
      <div class="description">
        <p>at MingdaoHS</p>
        <p>2020 / 09 / 11</p>
      </div>
      <!-- <p class="text-block-title">"FLIP!"</p> -->
    </div>
    <iframe width="700" height="315" src="https://www.youtube.com/embed/ZylCSKE9A24" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
  </section>
</template>

<script>
export default {
  
}
</script>

<style lang="scss" scoped>
.ted-youtube {
  display: flex;
  flex-direction: row;
  .text-block {
    width: calc(100% - 450px);
    margin-right: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    p {
      font-size: 1.4em;
      margin: 10px 0;
    }
    .description {

    }
    .text-block-title {
      margin: 30px 0 0 0;
      font-size: 2.5em;
      font-weight: 500;
    }
  }
}
</style>