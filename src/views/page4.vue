<template>
  <div class="page4 align-column-center">
    <nav
      class="navbar navbar-expand-lg navbar-dark fixed-top font-14px"
      style="background-color: #14072f"
    >
      <div class="container-fluid">
        <a class="navbar-brand" href="#/page4">科技藝術</a>
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
                學程
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a class="dropdown-item" href="http://aet.web.nthu.edu.tw/"
                    >學程介紹</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="http://aet.web.nthu.edu.tw/"
                    >修業規定</a
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
                  <a class="dropdown-item" href="http://aet.web.nthu.edu.tw/"
                    >學士班跨域專、 兼師資</a
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
                工作坊
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a class="dropdown-item" href="http://aet.web.nthu.edu.tw/"
                    >清華BB8大會串</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="http://aet.web.nthu.edu.tw/"
                    >3D Printer DIY 工作坊</a
                  >
                </li>
                <li>
                  <a class="dropdown-item" href="http://aet.web.nthu.edu.tw/"
                    >Fablab怪怪桌工作坊</a
                  >
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <div class="banner align-column-center slide-down">
      <img class="img-100vw" src="../assets/banner3.png" alt="banner" />
    </div>
    <div class="content align-column-center">
      <div
        class="recently-event padding-30px align-column-start align-self-start"
      >
        <h1 class="ml6">
          <span class="text-wrapper">
            <span class="letters label">近期事件 New post</span>
          </span>
        </h1>
        <div class="hr margin-top-bottom"></div>
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
    </div>
    <div class="footer align-column-center padding-15px">
      <div class="copyright align-column-center margin-top-bottom">
        <p>
          國立清華大學跨院碩「藝術與創新科技」組 | Tel:+886-3-5715131 #78802
        </p>
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
.dropdown-item,
.dropdown-menu {
  background-color: #14072f;
  color: rgba(255, 255, 255, 0.7);
  font-size: 14px;
}
.dropdown-item:hover,
.dropdown-menu:hover {
  background-color: #14072f;
  color: rgba(255, 255, 255, 0.9);
  font-size: 14px;
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
  height: 100%;
  overflow-y: scroll;
  scrollbar-width: none;
  border-radius: 10px;
}
.events-container::-webkit-scrollbar {
  display: none;
}
.events {
  background: rgba(29, 35, 65, 0.6);
  box-sizing: border-box;
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
</style>

<script>
export default {
  name: "Page4",
  data() {
    return {
      events: [
        {
          src: require("@/assets/page4/img1.jpg"),
          date: "2020.5.27",
          description: "從腦科學看藝術 – 謝仁俊教授演講",
          link: "https://art.nthu.edu.tw/?p=2044",
        },
        {
          src: require("@/assets/page4/img2.jpg"),
          date: "2020.4.1",
          description: "科技藝術策展人講座系列",
          link: "https://art.nthu.edu.tw/?p=2020",
        },
        {
          src: require("@/assets/page4/img3.jpg"),
          date: "2019.11.11",
          description: "互動藝術中的沉浸式即興創作",
          link: "https://art.nthu.edu.tw/?p=2002",
        },
        {
          src: require("@/assets/page4/img4.jpg"),
          date: "2019.10.23",
          description: "2019/11/1(五)跨院碩士學位學程(科技藝術組)面試通知",
          link: "https://art.nthu.edu.tw/?p=2017",
        },
        {
          src: require("@/assets/page4/img5.jpg"),
          date: "2019.10.19",
          description: "2019/10/28(一)跨院博士學位學程(科技藝術組)面試通知",
          link: "https://art.nthu.edu.tw/?p=2006",
        },
        {
          src: require("@/assets/page4/img6.jpg"),
          date: "2019.10.17",
          description: "11/4勝本雄一朗演講",
          link: "https://art.nthu.edu.tw/?p=1979",
        },
        {
          src: require("@/assets/page4/img7.jpg"),
          date: "2019.10.13",
          description: "清華大學【藝術學院大樓】建築比案終於出爐！",
          link: "https://art.nthu.edu.tw/?p=1966",
        },
        {
          src: require("@/assets/page4/img8.jpg"),
          date: "2019.10.03",
          description: "「科技藝術組」招生 (10/2~10/8報名)",
          link: "https://art.nthu.edu.tw/?p=1971",
        },
        {
          src: require("@/assets/page4/img9.jpg"),
          date: "2019.09.30",
          description: "跨院碩 – 推甄開始報名",
          link: "https://art.nthu.edu.tw/?p=1971",
        },
      ],
      isPlaying: false,
      event_below: false,
    };
  },
  created() {
    document.addEventListener("scroll", this.eventScroll);
    window.scrollTo(0, 0);
  },

  methods: {
    eventScroll() {
      this.fadeIn();
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
  },
};
</script>
