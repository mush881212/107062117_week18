<template>
  <div class="page3 align-column-center">
    <nav
      class="navbar navbar-expand-lg navbar-dark fixed-top font-14px"
      style="background-color: #14072f"
    >
      <div class="container-fluid">
        <a class="navbar-brand" href="#/page3">藝術學院學士班</a>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                id="navbarDropdownMenuLink"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                學士班
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=2"
                    >學士班簡介</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=69"
                    >學士班課程</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://ipta.nthu.edu.tw/?p=6607"
                    >藝術學院大樓</a
                  >
                </li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                id="navbarDropdownMenuLink"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                師資
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=30"
                    >學士班師資</a
                  >
                </li>
              </ul>
            </li>
            <li class="nav-item dropdown">
              <a
                class="nav-link dropdown-toggle"
                href="#"
                id="navbarDropdownMenuLink"
                role="button"
                data-bs-toggle="dropdown"
                aria-expanded="false"
              >
                科藝賞析
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=47"
                    >數位文創作品</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=43"
                    >互動藝術作品</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=45"
                    >動力藝術作品</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=52"
                    >聲音藝術作品</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://ipta.nthu.edu.tw/?page_id=49"
                    >科技表演藝術</a
                  >
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="banner align-column-center slide-down">
      <img class="img-100vw" src="../assets/banner4.png" alt="banner" />
    </div>
    <div class="content align-column-center">
      <div
        class="recent-event padding-30px align-column-start align-self-start"
      >
        <h1 class="ml6">
          <span class="text-wrapper">
            <span class="letters label">近期事件 New post</span>
          </span>
        </h1>
        <div class="hr"></div>
        <div class="events-container align-row-center">
          <div
            class="events margin align-column-center"
            v-for="(item, index) in events"
            :key="index"
          >
            <div class="img-event margin-top-bottom">
              <img v-bind:src="item.src" v-bind:alt="item.description" />
            </div>
            <div class="hr"></div>
            <div class="description align-row-center padding-15px">
              <a v-bind:href="item.link" target="_blank">
                {{ item.description }}
              </a>
            </div>
          </div>
        </div>
      </div>
      <div class="intro padding-30px align-column-center">
        <h1 class="ml6_1 align-self-end">
          <span class="text-wrapper">
            <span class="letters label">簡介 Introduction</span>
          </span>
        </h1>
        <div class="hr"></div>
        <div
          class="intro-item margin padding-30px align-column-center invisible"
          id="intro-item-1"
        >
          <p class="label">學士班特色</p>
          <div class="hr"></div>
          <p class="font-14px margin-top-bottom-5px">
            清華是國際頂尖科技大學，加上合校後的藝術學院，具備發展「科技藝術」的卓越條件。我們號召臺灣年輕一代的科技藝術學者專家，我們規劃有科技藝術跨域特別課程，並與業界合作推出創意跨域專題。你，不需猶豫，歡迎你的加入！
          </p>
        </div>
        <div
          class="intro-item margin padding-30px align-column-center invisible"
          id="intro-item-2"
        >
          <p class="label">核心能力</p>
          <div class="hr"></div>
          <p class="font-14px margin-top-bottom-5px">
            社會關懷與品格實踐能力<br />
            美感認知與經典欣賞能力<br />
            自然感知與創新發想能力<br />
            邏輯思辨與語文溝通能力<br />
            國際觀點與在地行動能力<br />
            資訊掌握與科技應用能力<br />
          </p>
        </div>
        <div
          class="intro-item margin padding-30px align-column-center invisible"
          id="intro-item-3"
        >
          <p class="label">學士班簡介</p>
          <div class="hr"></div>
          <p class="font-14px margin-top-bottom-5px">
            清華大學2018年成立藝術學院〝科技藝術〞跨域「學士班」。
            「科技藝術（TechArt）」是當代藝術的新形式創作也是國際藝
            術發展的重要趨勢，包含虛擬藝術、互動藝術、電腦動畫、電腦音樂、
            聲音藝術、科技性表演藝術、混合藝術、網路社群、創客藝術、仿生藝術
            、生物藝術、人工生命…等。在當代數位美學與數位藝術的基礎下，我們結
            合創新科技，如各種互動感測技術、虛擬實境、物聯網、人工智慧、大數據
            分析、基因工程…，把「科技」與「藝術」結合視為「未來文化學」，培養前
            瞻性、跨域研究與創作人才。因應未來產業的發展趨勢，創新科技與當代藝術
            結合之創作如雨後春筍。清華大學的是國內科學與科技的頂尖學府，對藝術學
            院發展「科技藝術」具有得天獨厚的優勢。本班師資除來自清華校內藝術學院、
            電資學院、工學院、生命科學院、人文社會等跨域教師外，我們也將聘進一群
            來自美國、歐洲與日本跨國與跨域的專業教師。也廣邀在臺灣在科技藝術創作
            領域最頂尖的業界團隊與藝術家加入我們的教學團隊，讓同學得到專業與多元
            的指導，並在共享學習、共享創意的環境裡，開創未來的產業，盡情發揮自己
            的潛能。
          </p>
        </div>
      </div>
    </div>
    <div class="footer align-column-center padding-15px">
      <div class="copyright align-column-center margin-top-bottom">
        <p>國立清華大學藝術學院學士班</p>
        <p>2020 Copyright ©</p>
      </div>
    </div>
  </div>
</template>
<style>
html,
body {
  margin: 0px;
  background-color: #14072f;
  color: rgba(255, 255, 255, 0.7);
  line-height: 24px;
  letter-spacing: 3px;
}
.ml6,
.ml6_1 {
  position: relative;
}

.text-wrapper {
  position: relative;
  display: inline-block;
  padding-top: 0.2em;
  padding-right: 0.05em;
  padding-bottom: 0.1em;
  overflow: hidden;
}

.letter {
  display: inline-block;
}
a {
  color: rgba(255, 255, 255, 0.6);
  text-decoration: none;
}
a:hover {
  color: rgba(255, 255, 255, 0.7);
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
.intro {
  background-image: linear-gradient(
    0,
    rgba(255, 255, 255, 0.3),
    rgba(70, 72, 167, 0.3)
  );
  width: 100%;
}
.intro-item {
  background: rgba(29, 35, 65, 0.8);
  box-sizing: border-box;
  border-radius: 10px;
  width: 80%;
  transform: scale(1);
  transition: all 0.2s ease-out;
}
.intro-item:hover {
  transform: scale(1.05);
  transition: all 0.2s ease-out;
  /* background: rgba(29, 35, 65, 0.8); */
  background: linear-gradient(
    0deg,
    rgba(122, 121, 235, 0.8) 0%,
    rgba(68, 60, 175, 0.8) 100%
  );
}

.recent-event {
  background-image: linear-gradient(
    0,
    rgba(70, 72, 167, 0.3),
    rgba(0, 0, 0, 0.5)
  );
  width: 100%;
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

.align-self-end {
  align-self: flex-end;
}
.align-self-start {
  align-self: flex-start;
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

.fade-in {
  animation: fade-in 1s;
}
.fade-down {
  animation: fade-down 1s;
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
@keyframes fade-down {
  0% {
    opacity: 0.2;
    -webkit-transform: translateY(-10%);
    transform: translateY(-10%);
  }
  100% {
    opacity: 1;
    -webkit-transform: translateY(0%);
    transform: translateY(0%);
  }
}
</style>

<script>
export default {
  name: "Page3",
  data() {
    return {
      events: [
        {
          src: require("@/assets/page3/img1.jpg"),
          description: "2021春之清華 – 藝術卓越獎 科技藝術類 甄選辦法",
          link: "https://art.nthu.edu.tw/?p=2044",
        },
        {
          src: require("@/assets/page3/img2.png"),
          description:
            "《那顆Ｇ1咻！》國立清華大學藝術學院學士班第一屆系展 得獎名單",
          link: "https://art.nthu.edu.tw/?p=2020",
        },
        {
          src: require("@/assets/page3/img3.jpg"),
          description: "2020春之清華 – 藝術卓越獎 科技藝術類 得獎名單",
          link: "https://art.nthu.edu.tw/?p=2002",
        },
        {
          src: require("@/assets/page3/img4.png"),
          description: "《那顆Ｇ1咻！》國立清華大學藝術學院學士班第一屆系展",
          link: "https://art.nthu.edu.tw/?p=2017",
        },
        {
          src: require("@/assets/page3/img5.jpg"),
          description: "2020藝術學院學士班春之清華獎學金 獲獎名單",
          link: "https://art.nthu.edu.tw/?p=2006",
        },
        {
          src: require("@/assets/page3/img6.jpg"),
          description: "春之清華—藝術卓越獎科技藝術類 甄選辦法",
          link: "https://art.nthu.edu.tw/?p=1979",
        },
        {
          src: require("@/assets/page3/img7.jpg"),
          description:
            "國立清華大學 藝術學院學士班 徵聘【助理教授級以上】專任教師1名",
          link: "https://art.nthu.edu.tw/?p=1966",
        },
        {
          src: require("@/assets/page3/img8.jpg"),
          description: "《 科技物件與人類幻象講座 Ⅸ》6/16 Tue",
          link: "https://art.nthu.edu.tw/?p=1971",
        },
      ],
      event_below: false,
      item_below1: false,
      item_below2: false,
      item_below3: false,
      isPlaying: false,
      isPlaying1: false,
    };
  },
  created() {
    document.addEventListener("scroll", this.eventScroll);
    window.scrollTo(0, 0);
  },

  methods: {
    eventScroll() {
      this.fadeIn();
      var item1 = document.getElementById("intro-item-1");
      var item2 = document.getElementById("intro-item-2");
      var item3 = document.getElementById("intro-item-3");
      if (window.scrollY >= 1300) {
        this.fadeOut(item3);
        this.item_below3 = true;
      } else if (window.scrollY < 1300) {
        this.removeFadeOut(item3);
        this.item_below3 = false;
      }
      if (window.scrollY >= 1000) {
        this.fadeOut(item2);
        this.item_below2 = true;
      } else if (window.scrollY < 1000) {
        this.removeFadeOut(item2);
        this.item_below2 = false;
      }
      if (window.scrollY >= 600) {
        this.fadeOut(item1);
        this.item_below1 = true;
      } else if (window.scrollY < 600) {
        this.removeFadeOut(item1);
        this.item_below1 = false;
      }
      /**************************** */
      if (window.scrollY > 100 && !this.isPlaying) {
        this.isPlaying = true;
        var textWrapper = document.querySelector(".ml6 .letters");
        textWrapper.innerHTML = textWrapper.textContent.replace(
          /\S/g,
          "<span class='letter'>$&</span>"
        );
        this.$anime
          .timeline({ loop: false })
          .add({
            targets: ".ml6 .letter",
            translateY: ["1.1em", 0],
            translateZ: 0,
            duration: 1500,
            delay: (el, i) => 50 * i,
          })
          .add({
            targets: ".ml6",
            opacity: 1,
            duration: 1000,
            easing: "easeOutExpo",
            delay: 1000,
          });
      } else if (window.scrollY < 10) {
        this.isPlaying = false;
      }

      if (window.scrollY >= 600 && !this.isPlaying1) {
        this.isPlaying1 = true;
        var textWrapper1 = document.querySelector(".ml6_1 .letters");
        textWrapper1.innerHTML = textWrapper1.textContent.replace(
          /\S/g,
          "<span class='letter'>$&</span>"
        );
        this.$anime
          .timeline({ loop: false })
          .add({
            targets: ".ml6_1 .letter",
            translateY: ["1.1em", 0],
            translateZ: 0,
            duration: 1500,
            delay: (el, i) => 50 * i,
          })
          .add({
            targets: ".ml6_1",
            opacity: 1,
            duration: 1000,
            easing: "easeOutExpo",
            delay: 1000,
          });
      } else if (window.scrollY < 600) {
        this.isPlaying1 = false;
      }
    },
    fadeIn() {
      var events = document.getElementsByClassName("events");
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
    },
    fadeOut(item) {
      item.classList.remove("invisible");
      item.classList.add("fade-down");
    },
    removeFadeOut(item) {
      item.classList.add("invisible");
      item.classList.remove("fade-down");
    },
  },
};
</script>
