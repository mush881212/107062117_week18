<template>
  <div class="page1 align-column-center">
    <nav
      class="navbar navbar-expand-lg navbar-dark fixed-top font-14px"
      style="background-color: #14072f"
    >
      <div class="container-fluid">
        <a class="navbar-brand" href="#/page1">藝設系</a>
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
                本系簡介
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="https://drive.google.com/file/d/1d7Ih2bWnIdtegdJip8UJQI9tNZgTOZZk/view"
                    >介紹影片</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12584.php?Lang=zh-tw"
                    >系所特色</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-16736.php?Lang=zh-tw"
                    >課程地圖</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12585.php?Lang=zh-tw"
                    >規章辦法</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-13704.php?Lang=zh-tw"
                    >表單下載</a
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
                系所成員
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12568.php?Lang=zh-tw"
                    >專任師資</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12569.php?Lang=zh-tw"
                    >兼任師資</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12570.php?Lang=zh-tw"
                    >行政助教</a
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
                獲獎成果
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12587.php?Lang=zh-tw"
                    >李澤藩教授美勞教育獎學金歷年得獎作品</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-12588.php?Lang=zh-tw"
                    >校內外競賽獲獎</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="http://artdesign.site.nthu.edu.tw/p/412-1104-13946.php?Lang=zh-tw"
                    >新一代設計展</a
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
                藝術空間
              </a>
              <ul
                class="dropdown-menu"
                aria-labelledby="navbarDropdownMenuLink"
              >
                <li>
                  <a
                    class="dropdown-item"
                    href="https://nthuartspace.wixsite.com/chushih-artspace"
                    >竹師藝術空間</a
                  >
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://nthuartspace.wixsite.com/chushih-artspace"
                  >
                    竹師藝術空間2館
                  </a>
                </li>
                <li>
                  <a
                    class="dropdown-item"
                    href="https://nthuartspace.wixsite.com/chushih-artspace"
                  >
                    澤藝術空間
                  </a>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <div class="banner align-column-center slide-down">
      <img class="img-100vw" src="../assets/banner1.png" alt="banner" />
    </div>
    <div class="content align-column-center">
      <div class="slide-container padding-30px align-column-center">
        <h1 class="ml6_2 align-self-start">
          <span class="text-wrapper">
            <span class="letters label">藝廊 Gallery</span>
          </span>
        </h1>
        <div class="hr margin-top-bottom"></div>
        <div class="slide-content padding-15px">
          <vue-glide
            :autoplay="false"
            :perView="1"
            :animationDuration="3000"
            :rewindDuration="800"
          >
            <vue-glide-slide
              class="slide align-column-center"
              v-for="(item, index) in slides"
              :key="index"
            >
              <p class="margin-5px-8px">
                {{ item.author }} 《{{ item.name }}》
              </p>
              <img
                class="img-80"
                v-bind:src="item.src"
                v-bind:alt="item.name"
              />
            </vue-glide-slide>
            <template slot="control">
              <button class="button margin-left-right" data-glide-dir="<">
                prev
              </button>
              <button class="button margin-left-right" data-glide-dir=">">
                next
              </button>
            </template>
          </vue-glide>
        </div>
      </div>
      <!---------------------------->
      <div class="recently-event padding-30px align-column-start">
        <h1 class="ml6 align-self-end">
          <span class="text-wrapper">
            <span class="letters label">近期事件 New post</span>
          </span>
        </h1>
        <div class="hr margin-top-bottom"></div>
        <div class="events-container align-column-center">
          <div
            class="event align-row-center padding-30px invisible"
            v-for="(item, index) in events"
            :key="index"
          >
            <div class="date">
              {{ item.date }}
              <a class="description" v-bind:href="item.link" target="_blank">
                {{ item.description }}
              </a>
            </div>
          </div>
        </div>
      </div>
      <!---------------------------->
      <div class="gallery align-column-center padding-30px">
        <h1 class="ml6_1 align-self-start">
          <span class="text-wrapper">
            <span class="letters label">藝術空間 Art area</span>
          </span>
        </h1>
        <div class="hr"></div>
        <div class="gallery-container align-row-center">
          <div
            class="gallery-event align-column-center margin flip-card"
            v-for="(item, index) in gallerys"
            :key="index"
          >
            <div class="flip-card-inner">
              <div class="flip-card-front padding-15px">
                <img
                  calss="margin-top-bottom"
                  v-bind:src="item.src"
                  v-bind:alt="item.name"
                />
                <p class="margin-top-bottom">
                  {{ item.gallery }}
                </p>
                <div class="hr"></div>
                <div class="align-column-center">
                  <p class="font-14px margin-5px-8px align-self-start">
                    展演名稱: {{ item.name }}
                  </p>
                  <p class="font-14px margin-5px-8px align-self-start">
                    日期: {{ item.date }}
                  </p>
                  <p class="font-14px margin-5px-8px align-self-start">
                    時間: {{ item.time }}
                  </p>
                </div>
              </div>
              <div class="flip-card-back padding-15px">
                <p class="margin-top-bottom">簡介</p>
                <div class="hr"></div>
                <p class="margin-5px-8px font-14px">
                  {{ item.description }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="footer align-column-center padding-15px">
      <div class="copyright align-column-center margin-top-bottom">
        <p>國立清華大學藝術與設計學系 Tel:03-5715131#72901、72903</p>
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
.button {
  /* background: linear-gradient(
    0deg,
    rgba(170, 169, 245, 0.6) 0%,
    rgba(89, 78, 242, 0.6) 100%
  ); */
  background: rgba(170, 169, 245, 0.6);
  border: 0px;
  border-radius: 10px;
  text-align: center;
  width: 100px;
  height: 40px;
  border-bottom: 5px solid rgba(107, 97, 247, 0.6);
}
.button:hover {
  animation: button-down 0.3s;
  transition: all 0.1s ease-out;
  -webkit-transform: translateY(10%);
  transform: translateY(10%);
  border-bottom: 0px solid rgba(70, 89, 182, 0.8);
  background-image: linear-gradient(
    to right top,
    #1e6ce2,
    #4473e9,
    #5c7bef,
    #7183f6,
    #838bfc
  );
}
.ml6,
.ml6_1,
.ml6_2 {
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
.recently-event {
  background-image: linear-gradient(
    0,
    rgba(70, 72, 167, 0.3),
    rgba(0, 0, 0, 0.5)
  );
  width: 100%;
}
.events-container {
  width: 90%;
  height: 500px;
  overflow-y: scroll;
  scrollbar-width: none;
  border-radius: 10px;
}
.events-container::-webkit-scrollbar {
  display: none;
}
.event {
  width: 80%;
  background: rgba(29, 35, 65, 0.6);
  box-sizing: border-box;
  border-radius: 10px;
}
.event:hover {
  box-shadow: 0 0 10px rgba(167, 189, 250, 0.72),
    0 0 20px rgba(167, 181, 250, 0.72), 0px 0px 30px rgba(167, 181, 250, 0.72);
  transition: all 0.5s ease-out;
  transform: translateY(-10px);
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
.gallery {
  background-image: linear-gradient(
    0,
    rgba(255, 255, 255, 0.3),
    rgba(70, 72, 167, 0.3)
  );
  width: 100%;
}
.gallery-container {
  border: rgba(255, 255, 255, 0.6);
  width: 90%;
  border-radius: 20px;
  overflow-y: scroll;
  scrollbar-width: none;
}
.gallery-container::-webkit-scrollbar {
  display: none;
}

.gallery-event {
  width: 500px;
  align-items: center;
  font-size: 18px;
  border-radius: 10px;
}

.gallery-event img {
  width: 90%;
  height: 200px;
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
.img-80 {
  width: 60%;
  max-height: 70%;
}
.slide-container {
  width: 100%;
  background-color: rgba(0, 0, 0, 0.5);
}
.slide-content {
  width: 50%;
  height: 400px;
  background-color: rgba(167, 181, 250, 0.4);
  border-radius: 10px;
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
@keyframes button-down {
  0% {
    -webkit-transform: translateY(0%);
    transform: translateY(0%);
    border-bottom: 5px solid rgba(70, 89, 182, 0.8);
  }
  100% {
    -webkit-transform: translateY(10%);
    transform: translateY(10%);
    border-bottom: 0px solid rgba(70, 89, 182, 0.8);
  }
}
.flip-card {
  perspective: 1000px; /* Remove this if you don't want the 3D effect */
  height: 450px;
}

/* This container is needed to position the front and back side */
.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

/* Do an horizontal flip when you move the mouse over the flip box container */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

/* Position the front and back side */
.flip-card-front,
.flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden; /* Safari */
  backface-visibility: hidden;
  background: rgba(57, 69, 130, 0.8);
  border-radius: 10px;
}

/* Style the back side */
.flip-card-back {
  transform: rotateY(180deg);
  background: rgba(29, 35, 65, 1);
}
</style>

<script>
import { Glide, GlideSlide } from "vue-glide-js";
export default {
  name: "Page1",
  data() {
    return {
      events: [
        {
          date: "2021-01-08",
          description: "2021藝術與設計新秀申請展徵件審查第二次徵件通過名單",
          link: "https://art.nthu.edu.tw/?p=2044",
        },
        {
          date: "2020-12-24",
          description: "國立清華大學 藝術與設計學系(創作組) 徵聘專任教師1名",
          link: "https://art.nthu.edu.tw/?p=2020",
        },
        {
          date: "2020-12-18",
          description: "110學年度學士班特殊選才(拾穗計畫)錄取名單(含報到須知)",
          link: "https://art.nthu.edu.tw/?p=2002",
        },
        {
          date: "2020-12-08",
          description: "國立清華大學 藝術與設計學系(設計組) 徵聘專任教師1名",
          link: "https://art.nthu.edu.tw/?p=2017",
        },
        {
          date: "2020-11-27",
          description: "2020國立清華大學藝術與設計學系研究生論文研討會",
          link: "https://art.nthu.edu.tw/?p=2006",
        },
        {
          date: "2020-11-13",
          description: "110學年度藝設系特殊選才複試程序表---創作組、設計組",
          link: "https://art.nthu.edu.tw/?p=1979",
        },
        {
          date: "2020-11-12",
          description: "110學年度碩士班甄試入學榜單",
          link: "https://art.nthu.edu.tw/?p=1966",
        },
        {
          date: "2020-11-12",
          description: "國立清華大學110學年度碩士班考試入學招生簡章公告",
          link: "https://art.nthu.edu.tw/?p=1971",
        },
      ],
      gallerys: [
        {
          gallery: "竹師藝術空間",
          name: "沙地 SAND LAND 劉致宏",
          date: "2020/12/15(二)~2021/01/08(五)",
          time: "週一至週五 10:00~17:00",
          src: require("@/assets/page1/gallery1.jpg"),
          description:
            "「他本來想談談自己對孔雀椰林的莫名愛戀…以及海洋對他情感上無所不在的魔幻影響。」--《午後の曳航》三島由紀夫。現場所見大面積的「沙」鋪設於原有地磚之上，延伸了「手-畫布」/「身體-空間」的繪畫關係，讓空間成為情感傳遞的介面，而保留原有的縫隙/間隔，除暗示沙地與「海」的邊界關係外，也將空間製造了另一「塗層/圖層」，使繪畫性的表現擴展為整體的情境閱讀。另外幾個部分則由裝置組成，利用現成物、光線/陰影、文字等轉化，藉由物件特質與符號語言的交疊，讓「畫面」在空間裡緩緩浮現，述說當少年面對人性、所處(孔洞這一側)現實世界的「回過頭來」的況味。",
        },
        {
          gallery: "澤-藝術空間",
          name: "永恆的瞬間-鄭又禎創作個展",
          date: "2020/12/07(一)~2021/01/01(五)",
          time: "週一至週五 10:00~17:00",
          src: require("@/assets/page1/gallery2.jpg"),
          description:
            "記憶會隨時間而褪色，只有把記憶化為無限的想像，才能化瞬間為永恆，因而有了〜永恆的瞬間。由於萬物都有靈性，各式精靈的影像常常出現，所見所想漫無邊際，創作的靈感不須細想，自由放空心隨意走，運用自然審美觀，讓佐品表達出自己喜歡的樣貌，於是形成了「放空表現技法」。由於遠古與現代的時空重叠，在異次元空間的夾縫中，物種壓縮形變往往湧現異於想像的無名，與萬物共榮共生，用簡單的素材表現虛實變換的重疊空間，運用各種抽象面塊擠壓扭曲排列組合，於是有了各式各樣的樹木精靈、岩石精靈以及多面向精靈等等，讓我們的世界處處充滿驚喜，相信未來會有更奇妙的作品等著您我去創造。",
        },
      ],
      isPlaying: false,
      isPlaying1: false,
      isPlaying2: false,
      event_below: false,
      [Glide.name]: "獲獎紀錄",
      [GlideSlide.name]: "GlideSlide",
      slides: [
        {
          name: "苞藏 / Hiden",
          src: require("@/assets/page1/img1_1.jpg"),
          author: "許馨文",
        },
        {
          name: "幸福的青鳥IV",
          src: require("@/assets/page1/img2_1.jpg"),
          author: "蔡函庭",
        },
        {
          name: "時間",
          src: require("@/assets/page1/img3_1.jpg"),
          author: "陳珊珊",
        },
        {
          name: "群聚關係",
          src: require("@/assets/page1/img4_1.jpg"),
          author: "張巧妤",
        },
        {
          name: "頂樓的發光搖擺-3",
          src: require("@/assets/page1/img5_1.jpg"),
          author: "林君晏",
        },
      ],
    };
  },
  created() {
    document.addEventListener("scroll", this.eventScroll);
    window.scrollTo(0, 0);
  },

  methods: {
    eventScroll() {
      this.fadeIn();
      if (window.scrollY > 10 && !this.isPlaying2) {
        this.isPlaying2 = true;
        var textWrapper2 = document.querySelector(".ml6_2 .letters");
        textWrapper2.innerHTML = textWrapper2.textContent.replace(
          /\S/g,
          "<span class='letter'>$&</span>"
        );
        this.$anime
          .timeline({ loop: false })
          .add({
            targets: ".ml6_2 .letter",
            translateY: ["1.1em", 0],
            translateZ: 0,
            duration: 1500,
            delay: (el, i) => 50 * i,
          })
          .add({
            targets: ".ml6_2",
            opacity: 1,
            duration: 1000,
            easing: "easeOutExpo",
            delay: 1000,
          });
      } else if (window.scrollY < 10) {
        this.isPlaying2 = false;
      }
      if (window.scrollY > 800 && !this.isPlaying) {
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
      } else if (window.scrollY < 800) {
        this.isPlaying = false;
      }

      if (window.scrollY >= 1200 && !this.isPlaying1) {
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
      } else if (window.scrollY < 1200) {
        this.isPlaying1 = false;
      }
    },
    fadeIn() {
      var events = document.getElementsByClassName("event");
      if (window.scrollY >= 800 && !this.event_below) {
        events.forEach((element) => {
          element.classList.remove("invisible");
          element.classList.add("fade-in");
        });
        this.event_below = true;
      } else if (window.scrollY < 800) {
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
