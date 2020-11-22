<template>
  <section class="extra-curricular" id="extra-curricular">
    <h3 class="section-header">Extracurricular Activity</h3>
    <div class="block-header">
      <a href="https://2019.meichuhackathon.org/"><img src="/images/mei-chu-hackathon-logo.png" width="70px"/></a>
      <div class="block-words">
        <h3 class="section-subheader" style="color: #404040;">7th Mei-Chu Hackathon</h3>
        <h3 class="section-subheader">President</h3>
      </div>
    </div>
    <div class="mei-chu-bg"></div>
    <p class="paragraph">{{paragraph}}</p>
    <div class="padding"></div>
    <div class="block-header">
      <a href="https://www.facebook.com/hackathontaiwanjunior"><img style="border-radius: 50%" src="/images/hackathon-tw-junior-logo.png" width="70px"/></a>
      <div class="block-words">
        <h3 class="section-subheader" style="color: #404040;">Hackathon Taiwan Junior</h3>
        <h3 class="section-subheader">Founder & President</h3>
      </div>
    </div>
    <!-- <div class="mei-chu-bg"></div> -->
  </section>
</template>

<script>
export default {
  data() {
    return {
      paragraph: `During my presidency, I reformed the organization from corporation-oriented to a more socially-minded focus. As the result,
      we start to hold six CS+X workshops, including on the topics of education, startup, media, city governence, etc. for both CS major and non-CS major students. Furthermore, in our final Hackathon festival, we collaborated with school, Hsinchu city government, and big techs such as Google, Amazon, and Logitech to give students opportunities to gain practical experience in solving real-life issues.`
    }
  }
}
</script>

<style lang="scss" scoped>
.extra-curricular {
  padding: 100px 0 0 0;
  .padding {
    height: 100px;
    width: 100%;
  }
  .section-header {
    color: #6495b5;
    font-size: 2em;
    margin-bottom: 40px;
  }
  .block-header {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-bottom: 20px;
    .block-words {
      display: flex;
      flex-direction: column;
      margin-left: 30px;
      .section-subheader {
        font-size: 1.7em;
      }
    }
  }
  .paragraph {
    margin-top: 25px;
  }
  .mei-chu-bg {
    background-image: url('/images/mei-chu-all.jpg');
    width: 100%;
    height: 300px;
    background-position: center;
    background-size: cover;
  }
}
</style>