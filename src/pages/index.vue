<template>
  <div class="container">
    <div class="main-text">
      <div class="main-text__overline">{{ $t("index.overline") }}</div>
      <h1 class="main-text__title">Min-Chi Chiang</h1>
      <div style="margin-bottom: 20px" class="main-text__description">mencher@berkerley.edu</div>
      <div class="main-text__description" v-html="$t('index.desciption')"></div>
    </div>

    <div class="about-me" id="element">
      <div class="about-me__text">
        <h2 class="about-me__title">{{ $t("index.aboutMe") }}</h2>
        <div v-html="$t('index.aboutMeText')"></div>
        <p class="biography-highlight">Interests</p>
        <section class="about-me__tech">
          <div>Cloud Computing / System Networking</div>
          <div>Parallel Computing / Distributed Computing</div>
          <div>MLSys</div>
          <div>DevOps</div>
        </section>
        <div style="margin-top: 20px">
          <span>[<a href="/files/MinChi_Chiang_EECS_2022.pdf">Resume</a>]</span>
          <span>[<a href="https://www.linkedin.com/in/mencher-chiang">Linkedin</a>]</span>
          <span>[<a href="https://github.com/Louis5499">Github</a>]</span>
        </div>
        <!-- <p style="margin-top: 15px" class="biography-highlight">Education</p> -->
        <!-- <section class="about-me__tech">
          <div>University of California, Berkeley</div>
          <div>Master of Engineering in EECS</div>
          <div class="special-label"><b>UC Berkeley College of Engineering Fung Excellence Scholarship</b></div>
        </section> -->
        <!-- <section class="about-me__tech" style="margin-top: 20px">
          <div>National Tsing Hua University (NTHU)</div>
          <div>B.S. in Computer Science</div>
          <div>Overall GPA: 3.95 / 4.30</div>
          <div>CS Major GPA: 4.05 / 4.30</div>
          <div class="special-label"><b>NTHU CS Outstanding Academic Achievement Award</b></div>
        </section> -->
      </div>
      <div class="about-me__photo">
        <img src="~/assets/icons/min_chi_compress.png" alt="Hans Felix" />
      </div>
    </div>

    <Education />
    <WorkExperience />
    <PublicationSector />
    <!-- <TedYoutube /> -->
    <ExtraCurricular />
    <SelectedProjects />
    <IndexContact />

    <div class="background">
      <h-icon name="background" width="300" height="300"></h-icon>
    </div>

    <div class="social">
      <a class="social__item" href="https:/www.linkedin.com/in/mencher-chiang" target="_blank">
        <h-icon name="linkedin" width="20" height="20"></h-icon>
      </a>
      <!-- <a class="social__item" href="https://twitter.com/hansfelixramos" target="_blank">
        <h-icon name="twitter" width="20" height="20"></h-icon>
      </a> -->
      <!-- <a class="social__item" href="https://stackoverflow.com/users/9176232/hans-felix-ramos?tab=profile" target="_blank">
        <h-icon name="stackoverflow" width="20" height="20"> </h-icon>
      </a> -->
      <a class="social__item" href="https://github.com/Louis5499" target="_blank">
        <h-icon name="github" width="20" height="20"> </h-icon>
      </a>
      <a class="social__item" href="https://medium.com/mencher-publication" target="_blank">
        <h-icon name="medium" width="20" height="20"> </h-icon>
      </a>
    </div>

    <footer class="footer">
      This is an academic website for Min-Chi Chiang to share his experiences, projects, publications. The style of this website is borrowed from &copy; Hans Felix.
    </footer>
  </div>
</template>

<script>
import IndexContact from "@/components/index/IndexContact";
import TedYoutube from "@/components/index/TedYoutube";
import PublicationSector from "@/components/index/PublicationSector";
import WorkExperience from "@/components/index/WorkExperience";
import ExtraCurricular from "@/components/index/ExtraCurricular";
import SelectedProjects from "@/components/index/SelectedProjects";
import Education from '@/components/index/Education.vue';

export default {
  components: {
    IndexContact,
    TedYoutube,
    PublicationSector,
    WorkExperience,
    ExtraCurricular,
    SelectedProjects,
    Education
  }
};
</script>

<style lang="scss">
.container {
  width: 100%;
  max-width: 1300px;
  padding: 0 150px;
  margin: 0 auto;

  @include mq($until: tablet) {
    padding: 10px 25px;
  }
}

a {
  color:#6495b5;
}

.main-text {
  height: calc(100vh - var(--toolbar-height));
  margin-top: var(--toolbar-height);
  display: flex;
  flex-direction: column;
  justify-content: center;

  &__overline {
    color: $main-color;
    font-family: "Inconsolata", monospace;
    font-size: 20px;
  }

  &__title {
    font-size: 75px;
    font-weight: 500;
    letter-spacing: -1px;
    margin: 0 0 15px;
  }

  &__description {
    max-width: 600px;
    font-size: 18px;
    line-height: 1.4;
  }
}

.about-me {
  padding: 130px 0 0 0;
  min-height: 50vh;
  display: grid;
  grid-template-columns: 60% 40%;

  .biography-highlight {
    font-weight: 600;
  }

  .about-me__tech {
    display: flex;
    flex-direction: column;
  }

  &__photo {
    align-self: center;
    justify-self: end;

    img {
      max-width: 250px;
      border-radius: 50%;
      // filter: grayscale(1);
      opacity: 0.75;
      transition: 0.2s all ease-in-out;
    }

    @include mq($until: tablet) {
      grid-row-start: 1;
      justify-self: center;

      img {
        max-width: 150px;
        margin: 10px;
      }
    }
  }

  &__text {
    align-self: center;
    justify-self: center;
    font-size: 17px;
    line-height: 1.4;

    p {
      margin-bottom: 15px;
    }
  }

  &__title {
    color: #6495b5;
    font-size: 1.8em;
    margin-bottom: 15px;
  }

  &__tech {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-gap: 5px;

    //TODO: Add custom class for this div
    div:before {
      content: "-";
      margin-right: 5px;
    }
    .special-label:before {
      content: "";
    }

    @include mq($until: tablet) {
      grid-template-columns: 1fr 1fr;
    }
  }

  @include mq($until: tablet) {
    grid-template-columns: auto;
    grid-template-rows: 1fr 1;
  }
}

.social {
  position: fixed;
  top: 0;
  left: 0;
  height: 100%;
  width: 100px;
  display: flex;
  flex-direction: column;
  justify-content: flex-end;
  align-items: center;
  padding-bottom: 50px;

  &__item {
    width: 40px;
    height: 40px;
    margin: 5px;
    border-radius: 50%;
    background: transparent;
    color: inherit;
    cursor: pointer;
    transition: 0.2s background ease-in-out;
    @include flex-and-center;

    &:hover {
      background-color: #0000001a;
    }
  }

  @include mq($until: tablet) {
    position: static;
    flex-direction: row;
    justify-content: center;
    width: 100%;
    padding: 20px 0 0px;
  }
}

.footer {
  min-height: 50px;
  @include flex-and-center;
}

.background {
  position: absolute;
  right: 0;
  top: 100vh;
  transform: translateY(-100%);
  opacity: 0.08;
}
</style>
