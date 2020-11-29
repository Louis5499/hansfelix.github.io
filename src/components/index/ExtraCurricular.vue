<template>
  <section class="extra-curricular" id="extra-curricular">
    <h3 class="section-header">Extracurricular Activity</h3>
    <div class="block-header">
      <a href="https://2019.meichuhackathon.org/"><img class="activity-logo" src="/images/mei-chu-hackathon-logo.png" width="70px"/></a>
      <div class="block-words">
        <h3 class="section-subheader" style="color: #404040;">7th Mei-Chu Hackathon</h3>
        <h3 class="section-subheader">President</h3>
      </div>
    </div>
    <div class="mei-chu-bg"></div>
    <div class="icons">
      <img class="icon" height="45px" src="/images/hackathon-cor-logo/rect/hccg.png" />
      <img class="icon" height="45px" src="/images/hackathon-cor-logo/sponsors/google-logo.png" />
      <img class="icon" height="45px" src="/images/hackathon-cor-logo/sponsors/aws-logo.png" />
      <img class="icon" height="45px" src="/images/hackathon-cor-logo/rect/logitech.png" />
      <img class="icon" height="45px" src="/images/hackathon-cor-logo/rect/kkbox.png" />
    </div>
    <p class="paragraph">{{mei_paragraph}}</p>
    <div class="padding"></div>
    <div class="block-header">
      <a href="https://www.facebook.com/hackathontaiwanjunior"><img class="activity-logo"  style="border-radius: 50%" src="/images/hackathon-tw-junior-logo.png" width="70px"/></a>
      <div class="block-words">
        <h3 class="section-subheader" style="color: #404040;">Hackathon Taiwan Junior</h3>
        <h3 class="section-subheader">Founder & President</h3>
      </div>
    </div>
    <div class="hackathon-junior-bg"></div>
    <p class="paragraph">{{junior_paragraph}}</p>
    <h3 class="talk-header">Talks / Lectures</h3>
    <div class="talk-blocks">
      <div v-for="(item, idx) in talk_list" class="talk-block" :key="idx">
        <div class="talk-block-headerbar">
          <h4 class="talk-block-header">{{item.name}}</h4><span style="margin-left: 20px">{{item.position}} at {{item.location}}</span>
        </div>
        <span>{{item.date}}</span>
        <div class="talk-block-links">
          <span v-if="item.video_links">[<a :href="item.video_links">video</a>]</span>
          <span v-if="item.slide_links">[<a :href="item.slide_links">slides</a>]</span>
          <span v-if="item.report_links">[<a :href="item.report_links">report</a>]</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      mei_paragraph: `During my presidency, I reformed the organization from corporation-oriented to a more socially-minded focus. As a result, we start to hold six CS+X workshops, including on the topics of education, startup, media, city governance, etc., for both CS major and non-CS major students. Furthermore, in our final Hackathon festival, we collaborated with the school, Hsinchu city government, and big techs such as Google, Amazon, and Logitech to give students opportunities to gain practical experience in solving real-life issues. Each collaborated corporation would bring up some real-life problems they encountered, and students need to choose their favorite company and topics they want to challenge. Within two days, each team needs to propose their idea, implement a minimum viable product, and finally present their result.`,
      junior_paragraph: `Hackathon Taiwan Junior is the first Hackathon event in Taiwan targeting high school students. We collaborated with Hackathon Taiwan in Taipei to found this new organization. As the founder and President of this organization, I negotiated with corporations and persuaded our principal sponsor to supply us with additional funding and resources. During the Hackathon festival, we conducted a series of workshops, ranging from Arduino, Quadrotor Aircraft to 3D Printer, and successfully collaborated with MakeSchool from Silicon Valley to co-hold the next Hackathon Event.`,
      talk_list: [
        {
          name: 'TED Talk',
          date: '2020/09',
          description: '',
          location: 'Taichung City',
          video_links: 'https://youtu.be/ZylCSKE9A24',
          slide_links: 'https://drive.google.com/file/d/1mbRVpwBO3pTWDz7jueratRBX5_sZBvmR/view?usp=sharing'
        },
        {
          name: 'Introduction to Data Science: Overview',
          date: '2020/07',
          description: '',
          position: 'Invited Lecturer',
          location: 'National Data Pilot Competition',
          slide_links: 'https://drive.google.com/file/d/1JmoJz54G3IGB3V6FiuZXoWoOdIBBtVyj/view?usp=sharing'
        },
        {
          name: 'Introduction to Container-Based System: Kubernetes',
          date: '2020/11',
          description: '',
          location: 'Taipei City',
          slide_links: 'https://drive.google.com/file/d/16dVKIxQ0TjWgmzCb8uPQLax7CsHVNktj/view?usp=sharing'
        },
        {
          name: 'CS Life Path: Heading to Research or Work',
          date: '2020/10',
          description: '',
          location: 'NTHU',
          slide_links: 'https://drive.google.com/file/d/1efATQFVIMJ81zbYrqDRyl9_P7IZ9Frc6/view?usp=sharing'
        },
        {
          name: 'Life Experience: Work Experience in Startup Industry',
          date: '2019/04',
          description: '',
          position: 'TechShare Workshops',
          location: 'Mei-Chu Hackathon',
          slide_links: 'https://drive.google.com/file/d/1Sgr71_3_sL5ekhCJhtA7gukAWpJ5VVQT/view?usp=sharing',
          report_links: 'https://medium.com/%E6%A2%85%E7%AB%B9%E9%BB%91%E5%AE%A2%E6%9D%BE/4-11-%E8%81%B7%E5%A0%B4%E8%88%87%E5%AD%B8%E7%94%9F%E7%94%9F%E6%B4%BB-%E6%B1%9F%E5%B2%B7%E9%8C%A1%E6%BC%94%E8%AC%9B%E5%9B%9E%E9%A1%A7-1264047916ec'
        }
      ]
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
  .icons {
    display: flex;
    height: 80px;
    align-items: center;
    justify-content: center;
    img {
      margin: 0 15px;
    }
  }
  .block-header {
    display: flex;
    flex-direction: row;
    align-items: center;
    margin-bottom: 20px;
    .activity-logo {
      transition: all .2s cubic-bezier(0.075, 0.82, 0.165, 1);
      &:hover {
        transform: scale(1.05);
      }
    }
    .block-words {
      display: flex;
      flex-direction: column;
      margin-left: 30px;
      .section-subheader {
        font-size: 1.7em;
      }
    }
  }
  .talk-header {
    font-size: 1.7em;
    margin: 30px 0;
  }
  .talk-blocks {
    display: flex;
    flex-direction: column;
    .talk-block {
      width: 100%;
      height: 90px;
      // background-color: #ccc;
      display: flex;
      flex-direction: column;

      transition: all .15s cubic-bezier(0.075, 0.82, 0.165, 1);
      // cursor: pointer;

      // &:hover {
      //   box-shadow: 3px 3px 8px rgba(0, 0, 0, 0.7);
      //   padding-left: 10px;
      // }

      .talk-block-headerbar {
        display: flex;
        flex-direction: row;
        align-items: flex-end;
      }
      .talk-block-header {
        font-size: 1.3em;
        font-weight: 500;
      }
      .talk-block-links {
        display: flex;
        flex-direction: row;
        margin: 5px 0 20px 0;
        span {
          margin-right: 20px;
        }
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
  .hackathon-junior-bg {
    background-image: url('/images/hackathon-junior.jpg');
    width: 100%;
    height: 300px;
    background-position: center;
    background-size: cover;
  }
}
</style>