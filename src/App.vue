<template>
  <div id="app">
   <Header></Header>
   <div id="eye-catch">
    <h1 class="eye-catch-title">機械にはできない仕事を</h1>
    <div class="news flex">
      <div class="news-white">
        <p class="date">2019/01/01</p>
        <p class="news-title">ニュースタイトルがここに入ります。3月の決算報告書</p>
      </div>
      <div class="news-black">
        <p>news</p>
      </div>
    </div>
   </div>
   <main id="main">
    <div id="about">
      <img src="./assets/mission-img.jpg" alt="#" class="about-img">
      <div class="about-contents">
        <h2>お客様のために進化する成長企業であり続ける</h2>
        <p>顧客主導型サービスを提供する企業として、お客様の会社経営に必要なサービスと情報を提供し続ける企業支援会社を目指します。企業が現在著効面している「勝ち残るため」の戦略を提供できる会社として、ホームページをはじめ、各種マーケティングをご提供いたします。</p>
        <button class="about-btn btn">ミッション詳細</button>
      </div>
    </div>
    <div id="service">
      <h2>service</h2>
      <div class="service-contents flex" v-for="(data,index) in serviceContents" :key="index" >
        <img class="service-img" :src="data.img" alt="#">
        <div class="service-text" :class="{'second':index === 1}">
          <div class="text-contents">
            <p class="service-title">{{data.title}}</p>
            <p>{{data.subTitle}}</p>
            <p class="text">{{data.text}}</p>
            <button class="service-btn btn">{{data.btn}}</button>
          </div>
        </div>
      </div>
    </div>
    <div id="information" class="flex">      
      <div class="info-contents" v-for="(data,index) in infoContents" :key="index">
        <img class="info-img" :src="data.img" alt="#">
        <div class="info-title">
          <h2 class="english-title">{{data.title}}</h2>
          <p class="japanese-title">{{data.subTitle}}</p>
       </div>
      </div>
    </div>
    <div id="FAQ">
      <table>
        <tr>
          <th class="faq-left">FAQ</th>
          <td class="faq-center">良くある質問</td>
        </tr>
      </table>
    </div>
    <div id="contact">
      <div class="contact-contents">
        <h2 class="english-title">contact</h2>
        <p class="japanese-title">お問い合わせ</p>
        <p class="message">お気軽にお問い合わせください。</p>
        <p class="sub-message">資料請求・お問い合わせなどなんでも気軽にお問い合わせください。お仕事のご連絡もお問い合わせページに飛んでいただいて、入力フォームにご記入お願いいたします。</p>
        <button class="contact-btn btn">お問い合わせへ</button>
      </div>
    </div>
  </main>  
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer";
export default {
  data() {
    return {
      infoContents :[
        {
          img: require("./assets/company.jpeg"),
          title: "company",
          subTitle: "会社概要"
        },
        {
          img: require("./assets/recruit.jpg"),
          title: "recruit",
          subTitle: "採用情報"
        },  
      ],
      serviceContents :[
        {
          img: require("./assets/service2.jpg"),
          title: "web制作事業",
          subTitle :"コーチングのミッション",
          text :"ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります",
          btn :"サービス詳細"
        },
        {
          img: require("./assets/service1.jpg"),
          title: "web制作事業",
          subTitle :"コーチングのミッション",
          text :"ユーザーが求める物を分析し、ユーザビリティを備えた最適なサイトを提供。建設業から美容、ブライダル、飲食店まで多種多様な業種の制作実績があります",
          btn :"サービス詳細"
        }
      ]
    };
  },
  components: {
    Header,
    Footer,
  },
};
</script>

<style scoped>
html, body, div, span, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
abbr, address, cite, code,
del, dfn, em, img, ins, kbd, q, samp,
small, strong, sub, sup, var,
b, i,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, figcaption, figure,
footer, header, hgroup, menu, nav, section, summary,
time, mark, audio, video {
    margin:0;
    padding:0;
    border:0;
    outline:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

body {
    line-height:1;
    box-sizing: border-box;
}

article,aside,details,figcaption,figure,
footer,header,hgroup,menu,nav,section {
    display:block;
}

nav ul {
    list-style:none;
}

blockquote, q {
    quotes:none;
}

blockquote:before, blockquote:after,
q:before, q:after {
    content:'';
    content:none;
}

a {
    margin:0;
    padding:0;
    font-size:100%;
    vertical-align:baseline;
    background:transparent;
}

/* change colours to suit your needs */
ins {
    background-color:#ff9;
    color:#000;
    text-decoration:none;
}

/* change colours to suit your needs */
mark {
    background-color:#ff9;
    color:#000;
    font-style:italic;
    font-weight:bold;
}

del {
    text-decoration: line-through;
}

abbr[title], dfn[title] {
    border-bottom:1px dotted;
    cursor:help;
}

table {
    border-collapse:collapse;
    border-spacing:0;
}

/* change border colour to suit your needs */
hr {
    display:block;
    height:1px;
    border:0;  
    border-top:1px solid #cccccc;
    margin:1em 0;
    padding:0;
}

input, select {
    vertical-align:middle;
}


.flex {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn {
  width: 140px;
  height: 35px;
  border: solid 1px #000;
}

#eye-catch {
  position: relative;
  width: 100%;
  height: 700px;
  background: url(./assets/eyecatch.jpg);
  background-size: cover;
  background-position: center;
}

.eye-catch-title {
  padding-top: 400px;
  padding-left: 10%;
  padding-right: 10%;
  color: #fff;
  font-size: 50px;
  font-family: italic;
}

.news {
  position: absolute;
  right: 0;
  bottom: 0;
  width: 50%;
  justify-content: flex-end;
}

.news-white {
  background-color: #fff;
  width: 80%;
  height: 60px;
}

.news-black {
  background-color: black;
  color: #fff;
  width: 20%;
  height: 60px;
  line-height: 60px;
  text-align: center;
}

.date {
  margin : 5px 0 0 5px;
  font-size: 12px;
}

.news-title {
  font-size: 13px;
  margin: 0 15px 0;
}

#about {
  color: #fff;
  background-color: black;
  height: 455px;
  position: relative;
}

.about-img {
  position: absolute;
  top: 100px;
  right: 5%;
  width: 600px;
  height: 400px;
}

.about-contents {
  position: absolute;
  top: 125px;  
  left: 20%;
  width: 50%;
}

.about-contents h2 {
  font-size: 30px;
}


.about-contents h2,
.about-contents p {
  margin-bottom: 30px;
}


#service {
  background: #cdcdcd;
  margin: 150px 0;
  width: 100%;
}

#service h2 {
  text-align: center;
  padding: 20px 0;
  font-size: 25px;
}

.service-img {
  height: 500px;
  width: 750px;
}

.service-text {
  box-sizing: border-box;
  height: 300px;
  width: 600px;
  background-color: #fff;
}

.text-contents {
  width: 75%;
  margin: 70px auto ;
  position: relative;
}

.service-text p {
  margin-bottom: 15px;
}


.service-title {
  font-weight: 700;
}

.service-btn {
  height: 35px;
  background-color: #fff;
  position: absolute;
  right: 0;
}

.service-contents {
  position: relative;
  padding-bottom: 220px;
}

.service-contents:nth-child(even) {
  flex-direction: row-reverse;
}

.service-text {
  position: absolute;
  left: 20%;
  right: 0;
  top: 100px;
}


.second {
  position: absolute;
  left: unset;
  right: 20%;
}

#information {
  width: 100%;
  text-align: center;
  background-color: #fff;
}



.info-contents {
  position: relative;
  width: 100%;
}

.info-img {
  width: 95%;
  height: 250px;
}

.info-title {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50% ,-50%);
  color: #fff;
}

.english-title {
  font-size: 25px;
  margin-bottom: 10px;
}

.japanese-title {
  font-size: 14px;
}

#FAQ {
  width: 75%;
  margin: 150px auto;
  background-color: black;
  color: #fff;
  padding: 50px 40px;  
}

table {
  width: 100%;
}

.faq-left {
  text-align: left;
  font-size: 25px;
}

.faq-center {
  width: 54%;
  font-size: 15px;
}

#contact {
  background:url(./assets/contact-bg.jpg);
  background-size: cover;
  height: 600px;
}

.contact-contents {
  width: 100%;
  text-align: center;
  color: #fff;
  padding: 140px 0;
}

.message {
  margin: 30px 0;
  font-size: 35px;
  letter-spacing: 2px;
}

.sub-message {
  width: 65%;
  margin:0 auto 30px;
  font-size: 15px;
}

.contact-btn {
  background-color: rgba(0, 0, 0, 0);
  border: #fff 1px solid;
  color: #fff;
}


.copy {
  color: #fff;
  background-color: black;
  text-align: center;
  width: 100%;
}

@media screen and (max-width: 480px) {
  
  .eye-catch-title {
    font-size: 60px;
    text-align: center;
    width: 80%;
    padding-top: 50%;
    margin: 0 auto;
  }

  .news {
    width: 100%;
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;  
  }

  #about {
  position: relative;
  width: 100%;
  height: 455px;
  padding: 40px 0;
}

 .about-img {
  position: absolute;
  top: unset;
  bottom:  -40px;
  width: 40%;
  height: auto;
}

.about-contents {
  position: initial;
  width: 70%;
  margin: 0 auto;
}

.about-contents h2 {
  font-size: 30px;
  letter-spacing: 2px;
  line-height: 40px;
}

.about-contents p {
  line-height: 26px;
}


.about-contents h2,
.about-contents p {
  margin-bottom: 30px;
}

.about-btn {
  width: 140px;
  height: 35px;
}

#service {
  width: 100%;
  margin: 50px auto;
}


.service-contents {
  display: block;
  position: initial;
  padding-bottom: 60px;
  margin: 0 auto;
  width: 90%;
}

.service-img {
  height: 250px;
  width: 100%;
}

.service-text {
  position: unset;
  width: 100%;
  height: 300px;
  padding: 20px;
}

.text-contents {
  width: 90%;
  margin: 0 auto;
  position: relative;
}

.service-text p {
  margin-bottom: 10px;
  line-height: 25px;
}


.service-btn {
  width: 140px;
  height: 40px;
  position: absolute;
  right: 0;  
}

#information {
  display: block;
}

.info-img {
  width: 100%;
}

.english-title {
  font-size: 40px;
}

#FAQ {
  width: 75%;
  margin: 0 auto;
  background-color: black;
  color: #fff;
  padding: 50px 40px;  
}

#FAQ{
  margin: 50px auto;
}

.faq-center {
  width: auto;
}

#contact {
  height: auto;
}

.contact-contents {
  width: 70%;
  margin: 0 auto;
  padding: 40px 0 ;
}


.sub-message {
  width: 100%;
  letter-spacing: 2px;
  line-height: 16px;
}

}
</style>
