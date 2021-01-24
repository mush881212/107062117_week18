<template>
  <div class="home align-column-center">
    <el-menu
      class="el-menu align-self-start"
      mode="horizontal"
      @select="handleSelect"
      background-color="#14072F"
      text-color="rgba(255, 255, 255, 0.7)"
      active-text-color="rgba(255, 255, 255, 1)"
    >
      <el-submenu index="1">
        <template slot="title">Home</template>
        <el-submenu index="2">
          <template slot="title">關於學院</template>
          <el-menu-item index="2-1"
            ><a href="https://art.nthu.edu.tw/?page_id=51" target="_blank"
              >學院簡介</a
            ></el-menu-item
          >
          <el-menu-item index="2-2"
            ><a href="https://art.nthu.edu.tw/?page_id=54" target="_blank"
              >未來展望</a
            ></el-menu-item
          >
          <el-menu-item index="2-3"
            ><a href="http://oga.nthu.edu.tw/school2.php" target="_blank"
              >姐妹學校</a
            ></el-menu-item
          >
        </el-submenu>
        <el-submenu index="3">
          <template slot="title">學院師資</template>
          <el-menu-item index="3-1"
            ><a href="https://art.nthu.edu.tw/?page_id=819" target="_blank"
              >榮譽院長</a
            ></el-menu-item
          >
          <el-menu-item index="3-2"
            ><a href="https://art.nthu.edu.tw/?page_id=893" target="_blank"
              >歷任院長</a
            ></el-menu-item
          >
          <el-menu-item index="3-3"
            ><a href="https://art.nthu.edu.tw/?page_id=143" target="_blank"
              >現任院長/行政人員</a
            ></el-menu-item
          >
          <el-menu-item index="3-4"
            ><a href="http://music.site.nthu.edu.tw/?Lang=zh-tw" target="_blank"
              >音樂系專兼任師資</a
            ></el-menu-item
          >
          <el-menu-item index="3-5"
            ><a
              href="http://artdesign.site.nthu.edu.tw/?Lang=zh-tw"
              target="_blank"
              >藝設系專兼任師資</a
            ></el-menu-item
          >
          <el-menu-item index="3-6"
            ><a href="http://ipta.nthu.edu.tw/?page_id=30" target="_blank"
              >學士班專兼任師資</a
            ></el-menu-item
          >
        </el-submenu>
        <el-submenu index="4">
          <template slot="title">榮譽榜</template>
          <el-menu-item index="4-1"
            ><a href="https://art.nthu.edu.tw/?page_id=1445" target="_blank"
              >教師獲獎</a
            ></el-menu-item
          >
          <el-menu-item index="4-2"
            ><a href="https://art.nthu.edu.tw/?page_id=1855" target="_blank"
              >春之獎學金</a
            ></el-menu-item
          >
          <el-menu-item index="4-3"
            ><a href="https://art.nthu.edu.tw/?page_id=1858" target="_blank"
              >春之卓越獎</a
            ></el-menu-item
          >
          <el-menu-item index="4-4"
            ><a href="https://art.nthu.edu.tw/?page_id=269" target="_blank"
              >學生獲獎</a
            ></el-menu-item
          >
        </el-submenu>
        <el-submenu index="5">
          <template slot="title">活動花絮</template>
          <el-menu-item index="5-1"
            ><a href="https://art.nthu.edu.tw/?page_id=130" target="_blank"
              >國際交流</a
            ></el-menu-item
          >
        </el-submenu>
      </el-submenu>
    </el-menu>
    <div class="banner align-column-center slide-down">
      <img class="img-100vw" src="../assets/banner.png" alt="banner" />
    </div>
    <div class="content align-column-center">
      <div
        class="recently-event padding-30px align-column-start align-self-start"
      >
        <p class="label">近期事件</p>
        <div class="hr"></div>
        <div class="events-container align-row-center">
          <div
            class="events margin align-column-center invisible"
            v-for="(item, index) in events"
            :key="index"
          >
            <div class="img-event margin-top-bottom">
              <img v-bind:src="item.src" v-bind:alt="item.description" />
            </div>
            <div class="hr"></div>
            <div class="date align-self-end margin-5px-8px">
              {{ item.date }}
            </div>
            <div class="description align-row-center padding-15px">
              <a v-bind:href="item.link" target="_blank">{{
                item.description
              }}</a>
            </div>
          </div>
        </div>
      </div>
      <div class="outside-web align-column-center">
        <p class="align-self-end label margin-left-right">系所介紹</p>
        <div class="hr align-self-end margin-left-right"></div>
        <div class="o-container align-column-center margin">
          <div
            class="o-event align-row-center padding-15px translate"
            v-for="(item, index) in oEvents"
            :key="index"
            :class="item.color"
            v-on:click="redirect(index)"
          >
            {{ item.label }}
          </div>
        </div>
      </div>
      <div class="contact align-row-center margin-top-bottom">
        <input
          v-for="(item, index) in socialMedia"
          :key="index"
          type="image"
          class="btn padding-15px img-8vw"
          v-bind:src="item.src"
          v-bind:name="item.name"
          v-bind:id="item.name"
          v-on:click="directTo(item.name)"
        />
      </div>
    </div>
    <div class="footer align-column-center padding-15px">
      <div class="others align-row-center margin-top-bottom">
        <a
          v-for="(item, index) in others"
          :key="index"
          class="margin-left-right margin-top-bottom-5px font-14px"
          v-bind:href="item.link"
          target="_blank"
        >
          {{ item.name }}
        </a>
      </div>
      <div class="copyright align-column-center margin-top-bottom">
        <p>國立清華大學藝術學院 Tel:+886-3-5715131 #78801</p>
        <p>2020 Copyright ©</p>
      </div>
    </div>
  </div>
</template>
<style scoped>
html,
body {
  margin: 0px;
  background-color: #14072f;
  color: rgba(255, 255, 255, 0.7);
  line-height: 24px;
  letter-spacing: 3px;
}
a {
  color: rgba(255, 255, 255, 0.6);
  text-decoration: none;
}
a:hover {
  color: rgba(255, 255, 255, 0.7);
}
.btn:hover {
  transform: scale(0.9);
  transition: all 0.2s ease-out;
}
.hr {
  width: 100%;
  height: 1px;
  border-top: 1px solid rgba(176, 187, 245, 0.6);
}

.banner {
  width: 100%;
}
.content {
  background-image: url("../assets/bg.png");
  background-repeat: no-repeat;
  background-position: center top;
  background-size: 100vw;
  width: 100vw;
  height: auto;
}
.recently-event {
  background-image: linear-gradient(
    0,
    rgba(70, 72, 167, 0.3),
    rgba(0, 0, 0, 0.5)
  );
}
.events-container {
  width: 100%;
  height: 500px;
  overflow-y: scroll;
  scrollbar-width: none;
}
.events-container::-webkit-scrollbar {
  display: none;
}
.events {
  background: rgba(29, 35, 65, 0.6);
  box-sizing: border-box;
  border-radius: 10px;
  width: 250px;
  height: 250px;
}
.events:hover {
  box-shadow: 0 0 10px rgba(167, 189, 250, 0.72),
    0 0 20px rgba(167, 181, 250, 0.72), 0px 0px 30px rgba(167, 181, 250, 0.72);
  transition: all 0.5s ease-out;
  transform: translateY(-10px);
}
.img-event {
  width: 90%;
  height: 100px;
  overflow: hidden;
  border-radius: 10px;
}
.img-event img {
  max-width: 100%;
}
.label {
  font-size: 20px;
}
.date {
  font-size: 7px;
}
.description {
  font-size: 15px;
}
.outside-web {
  width: 100vw;
  background-image: linear-gradient(
    0,
    rgba(255, 255, 255, 0.3),
    rgba(70, 72, 167, 0.3)
  );
}
.o-container {
  border: rgba(255, 255, 255, 0.6);
  width: 90%;
  border-radius: 20px;
  overflow: hidden;
}
.o-container::-webkit-scrollbar {
  display: none;
}

.o-event {
  width: 100%;
  height: 150px;
  background: rgba(57, 69, 130, 0.72);
  align-items: center;
  position: relative;
  font-size: 18px;
  cursor: pointer;
}
.o-event:hover {
  animation: bounce 1s;
  transition: all 0.3s ease-out;
}

.align-self-end {
  align-self: flex-end;
}
.align-self-start {
  align-self: flex-start;
}

.others {
  width: 60%;
  flex-direction: row-reverse;
}
.copyright {
  width: 100%;
  color: rgba(255, 255, 255, 0.6);
  font-size: 12px;
}
.no-margin {
  margin: 0px;
}
.margin-left-right {
  margin-left: 20px;
  margin-right: 20px;
}
.margin-top-bottom {
  margin-top: 15px;
  margin-bottom: 15px;
}
.margin-top-bottom-5px {
  margin-top: 5px;
  margin-bottom: 5px;
}
.margin {
  margin: 20px;
}
.margin-5px-8px {
  margin-top: 5px;
  margin-left: 8px;
  margin-right: 8px;
  margin-bottom: 5px;
}

.padding-15px {
  padding: 15px;
}
.padding-30px {
  padding: 30px;
}

.img-8vw {
  max-width: 8vw;
  max-height: 8vw;
}
.img-100vw {
  width: 100vw;
}
.align-column-center {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.align-column-start {
  display: flex;
  flex-direction: column;
  align-items: start;
}
.align-row-center {
  display: flex;
  flex-direction: row;
  justify-content: center;
  flex-wrap: wrap;
}
.align-row-nowrap {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.red:hover {
  background-color: rgba(250, 119, 119, 0.5);
}
.orange:hover {
  background-color: rgba(250, 182, 119, 0.5);
}
.yellow:hover {
  background-color: rgba(247, 237, 150, 0.5);
}
.green:hover {
  background-color: rgba(119, 250, 189, 0.5);
}
.blue:hover {
  background-color: rgba(119, 235, 250, 0.5);
}
.purple:hover {
  background-color: rgba(121, 119, 250, 0.5);
}

.fade-in {
  animation: fade-in 1s;
}
.slide-in {
  animation: slide-in 1s;
}
.slide-out {
  animation: slide-out 1s;
}
.slide-down {
  animation: slide-down 1s;
  transition: all 0.2s ease-out;
}
.invisible {
  opacity: 0;
}
.translate {
  -webkit-transform: translateX(-100%);
  transform: translateX(-100%);
}
.font-14px {
  font-size: 14px;
}

@keyframes bounce {
  0%,
  20%,
  60%,
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }

  40% {
    -webkit-transform: translateY(-10px);
    transform: translateY(-10px);
  }

  80% {
    -webkit-transform: translateY(-5px);
    transform: translateY(-5px);
  }
}
@keyframes slide-in {
  0% {
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
  }
  100% {
    -webkit-transform: translateX(0%);
    transform: translateX(0%);
  }
}
@keyframes slide-out {
  0% {
    -webkit-transform: translateX(0%);
    transform: translateX(0%);
  }
  100% {
    -webkit-transform: translateX(-100%);
    transform: translateX(-100%);
  }
}
@keyframes slide-down {
  0% {
    -webkit-transform: translateY(-100%);
    transform: translateY(-100%);
  }
  100% {
    -webkit-transform: translateY(0%);
    transform: translateY(0%);
  }
}
@keyframes fade-in {
  0% {
    opacity: 0.2;
    -webkit-transform: translateY(10%);
    transform: translateY(10%);
  }
  100% {
    opacity: 1;
    -webkit-transform: translateY(0%);
    transform: translateY(0%);
  }
}
.el-menu.el-menu--horizontal {
  border: none;
  font-family: "ZCOOL QingKe HuangYou", "Sue Ellen Francisco", cursive;
  position: fixed;
  z-index: 99999;
  width: 100%;
}
</style>

<script>
export default {
  name: "Home",
  data() {
    return {
      activeIndex: "1",
      events: [
        {
          src: require("@/assets/timthumb.png"),
          date: "9.24",
          description: "清華大學藝設系研究生論文研討會 – 徵稿",
          link: "https://art.nthu.edu.tw/?p=2044",
        },
        {
          src: require("@/assets/img2.png"),
          date: "7.31",
          description: "清華藝術學報",
          link: "https://art.nthu.edu.tw/?p=2020",
        },
        {
          src: require("@/assets/img8.png"),
          date: "7.22",
          description: "藝設系設計組-異質對話",
          link: "https://art.nthu.edu.tw/?p=2002",
        },
        {
          src: require("@/assets/img3.png"),
          date: "7.3",
          description: "華山烏梅劇場「Face to face」實驗性跨領域展演",
          link: "https://art.nthu.edu.tw/?p=2017",
        },
        {
          src: require("@/assets/img7.png"),
          date: "6.11",
          description: "藝術學院-畢業典禮",
          link: "https://art.nthu.edu.tw/?p=2006",
        },
        {
          src: require("@/assets/img4.png"),
          date: "4.27",
          description: "藝設系學生獲獎－第14屆福爾摩沙珠寶設計教育推廣競賽",
          link: "https://art.nthu.edu.tw/?p=1979",
        },
        {
          src: require("@/assets/img5.png"),
          date: "4.1",
          description: "清明連假後防疫措施",
          link: "https://art.nthu.edu.tw/?p=1966",
        },
        {
          src: require("@/assets/img6.png"),
          date: "4.1",
          description: "科技藝術策展人講座系列 Metabolism at Contemporary",
          link: "https://art.nthu.edu.tw/?p=1971",
        },
      ],
      oEvents: [
        {
          label: "藝設系",
          link: "../views/page1.vue",
          color: "red",
        },
        {
          label: "音樂系",
          link: "../views/page2.vue",
          color: "orange",
        },
        {
          label: "科技藝術學院學士班",
          link: "../views/page3.vue",
          color: "yellow",
        },
        {
          label: "藝術與創新科技碩士學程",
          link: "../views/page4.vue",
          color: "green",
        },
        {
          label: "春之藝術專題講座",
          link: "http://art.nthu.edu.tw/artspeech",
          color: "blue",
        },
        {
          label: "科技藝術研究中心",
          link: "http://techart.nthu.edu.tw/",
          color: "purple",
        },
      ],
      others: [
        { name: "Top News", link: "https://art.nthu.edu.tw/?cat=1" },
        { name: "合作交流", link: "https://art.nthu.edu.tw/?cat=8" },
        { name: "國際交流", link: "https://art.nthu.edu.tw/?cat=5" },
        { name: "學生成就", link: "https://art.nthu.edu.tw/?cat=7" },
        { name: "學院公告", link: "https://art.nthu.edu.tw/?cat=9" },
        { name: "學院活動", link: "https://art.nthu.edu.tw/?cat=4" },
        { name: "招生訊息", link: "https://art.nthu.edu.tw/?cat=6" },
      ],
      socialMedia: [
        {
          name: "facebook",
          src: "https://img.icons8.com/doodle/48/000000/facebook-new.png",
        },
        {
          name: "email",
          src: "https://img.icons8.com/doodle/48/000000/apple-mail.png",
        },
        {
          name: "twitter",
          src: "https://img.icons8.com/doodle/48/000000/twitter-circled.png",
        },
      ],
      event_below: false,
      oevent_below: [false, false, false, false, false, false, false],
      banner_below: false,
    };
  },
  created() {
    document.addEventListener("scroll", this.eventScroll);
  },

  methods: {
    directTo(str) {
      if (str == "facebook")
        window.location.href = "https://www.facebook.com/nthuarts";
      else if (str == "email") {
        var email = "coa@my.nthu.edu.tw;";
        var subject = "Hi";
        var emailBody = "你好!";
        var attach = "art.nthu.edu.tw";
        window.location.href =
          "mailto:" +
          email +
          "?subject=" +
          subject +
          "&body=" +
          emailBody +
          "attach=" +
          attach;
      } else window.location.href = "https://twitter.com/twitter";
    },
    redirect(index) {
      console.log(index);
      switch (index) {
        case 0:
          this.$router.push("/page1");
          break;
        case 1:
          this.$router.push("/page2");
          break;
        case 2:
          this.$router.push("/page3");
          break;
        case 3:
          this.$router.push("/page4");
          break;
      }
    },
    handleSelect(key, keyPath) {
      console.log(key, keyPath);
    },

    eventScroll() {
      var events = document.getElementsByClassName("events");
      var oevents = document.getElementsByClassName("o-event");

      if (window.scrollY >= 100 && !this.event_below) {
        events.forEach((element) => {
          element.classList.remove("invisible");
          element.classList.add("fade-in");
        });
        this.event_below = true;
      } else if (window.scrollY < 10) {
        events.forEach((element) => {
          element.classList.add("invisible");
          element.classList.remove("fade-in");
        });
        this.event_below = false;
      }

      var y_value = [700, 850, 1000, 1150, 1300, 1450, 1600];
      var i = 0;
      oevents.forEach((element) => {
        if (!this.oevent_below[i]) {
          if (window.scrollY >= y_value[i]) {
            element.classList.remove("translate");
            element.classList.add("slide-in");
            setTimeout(() => {
              element.classList.remove("slide-in");
            }, 1000);
            this.oevent_below[i] = true;
          }
        } else {
          if (window.scrollY < y_value[i]) {
            element.classList.add("slide-out");
            element.classList.add("translate");
            setTimeout(() => {
              element.classList.remove("slide-out");
            }, 1000);
            this.oevent_below[i] = false;
          }
        }
        i++;
      });
    },
  },
};
</script>
