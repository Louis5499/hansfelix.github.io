<template>
  <section class="education-sector" id="education-sector">
    <h3 class="section-header">Education</h3>
    <div class="school-banner">
      <img class="logo" src="~/assets/icons/uc-logo.png">
      <div class="school-info">
        <h3 class="school-header">University of California, Berkeley</h3>
        <h4 class="school-department">Master of Engineering in Electrical Engineering & Computer Science (EECS)</h4>
        <div class="special-label">Award: <b>UC Berkeley College of Engineering Fung Excellence Scholarship</b></div>
      </div>
    </div>
    <div class="school-banner">
      <img class="logo" src="~/assets/icons/nthu-logo.png">
      <div class="school-info">
        <h3 class="school-header">National Tsing Hua University (NTHU)</h3>
        <h4 class="school-department">Bachelor of Science in Computer Science (CS)</h4>
        <div>Overall GPA: 3.95 / 4.30</div>
        <div>CS Major GPA: 4.05 / 4.30</div>
        <div class="special-label">Award: <b>Outstanding Academic Achievement Award</b></div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
    }
  }
}
</script>

<style lang="scss" scoped>
.education-sector {
  padding: 50px 0 0 0;
  .section-header {
    color: #6495b5;
    font-size: 2em;
    margin-bottom: 15px;
  }
  .school-banner {
    display: flex;
    flex-direction: row;
    margin: 60px 0;
    .logo {
      width: 100px;
      height: 100px;
    }
    .school-info {
      display: flex;
      flex-direction: column;
      height: 100px;
      margin-left: 30px;
      justify-content: center;
    }
    .school-header {
      font-size: 1.2em;
      margin-bottom: 10px;
    }
    .school-department {
      font-size: 1em;
      font-weight: 500;
      margin-bottom: 20px;
    }
  }
}
</style>