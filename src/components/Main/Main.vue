<template>
  <section class="main">
    <article class="post main__post">
      <div class="post__inner">
        <div class="post__item">
          <img
            src="../../assets/images/Image.png"
            alt=""
            class="post__immage"
          />
          <h2 class="post__title">
            14 · Party people on the image above!
          </h2>
          <div class="post__data">
            <time datetime="2011-12-11" class="post__time">15 Dec, 2011</time>
            &nbsp;|&nbsp;
            <ul class="hashtag post__hashtegs">
              <li class="hashtag__item">
                <a href="hashtag__link">Dance</a>
              </li>
              &nbsp;·&nbsp;
              <li class="hashtag__item">
                <a href="hashtag__link">Party</a>
              </li>
              &nbsp;·&nbsp;
              <li class="hashtag__item">
                <a href="hashtag__link">People</a>
              </li>
            </ul>
            &nbsp;|&nbsp;
            <div class="post__comments-count">2 Comments</div>
          </div>
          <div class="post__text">
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis
              impedit tenetur veritatis magni, mollitia ipsa obcaecati alias?
              Dolorum officia corporis vitae, praesentium, sequi quam excepturi
              nisi voluptatum aperiam porro, repellat ut non deleniti obcaecati
              perspiciatis iure pariatur illum maiores ullam sunt nobis.
              Molestiae, pariatur nihil voluptate tenetur odio repellat mollitia
              dolorem, maiores itaque deserunt libero culpa aliquid commodi
              facere saepe vero assumenda deleniti soluta vitae a temporibus aut
              necessitatibus. Soluta possimus minus facere excepturi placeat
              sint eaque error. Magnam ab rem, vitae sit similique nisi
              laudantium, suscipit, reprehenderit repellat provident minus!
              Quaerat nisi error explicabo dolorum quae aliquid doloremque
              facilis.
            </p>
            <br />
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae,
              libero. Suscipit magnam omnis beatae id ipsam nam ipsa asperiores
              porro voluptatibus soluta tempora exercitationem explicabo nostrum
              sequi, ut voluptates illo.
            </p>
            <div class="post__socials">
              Liked it? Share it!
              <div class="post__social-wrapper">
                <a href="" class="post__social"></a>
                <a href="" class="post__social"></a>
              </div>
            </div>
          </div>
        </div>
        <div class="comment-wrapper">
          <div class="comment">
            <img
              src="../../assets/images/Avatar_1.png"
              alt=""
              class="comment__img"
            />
            <div class="comment__inner">
              <p class="comment__paragraph">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Commodi, deleniti. Consectetur repellat quisquam molestias ipsum
                illo sit voluptatibus enim porro! Enim odio eos pariatur
                explicabo tenetur dolores sapiente? Quidem in nulla quaerat
                maxime animi! Assumenda sint nesciunt atque expedita quos porro
                eius cum repudiandae libero beatae nemo amet, excepturi adipisci
                aspernatur quasi voluptas dolore, est magnam at. At, fuga
                distinctio ipsa praesentium dolores necessitatibus quibusdam
                delectus harum facilis, alias similique sint quas corporis fugit
                id explicabo, repudiandae laborum temporibus odit?
              </p>
              <div class="comment__data">
                posted on
                <time datetime="2011-12-15"> 15 Dec, 2011 </time>
                <span class="comment__from">by Lucy</span>
              </div>
            </div>
          </div>
          <div class="comment">
            <img
              src="../../assets/images/Avatar_2.png"
              alt=""
              class="comment__img"
            />
            <div class="comment__inner">
              <p class="comment__paragraph">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                Commodi, deleniti. Consectetur repellat quisquam molestias ipsum
                illo sit voluptatibus enim porro! Enim odio eos pariatur
                explicabo tenetur dolores sapiente? Quidem in nulla quaerat
                maxime animi!
              </p>
              <div class="comment__data">
                posted on
                <time datetime="2011-12-15"> 15 Dec, 2011 </time>
                <span class="comment__from">by Jake</span>
              </div>
            </div>
          </div>
        </div>
        <h2 class="title2 comment__title">post your<br /></h2>
        <div class="form comment__form">
          <div class="form__item">
            <label for="email">name:</label>
            <input class="input" type="text" id="name" name="name" required />
          </div>
          <div class="form__item">
            <label for="email">email:</label>
            <input
              class="input"
              type="email"
              id="email"
              name="email"
              pattern=".+@gmail.com"
              required
            />
          </div>
          <div class="form__item">
            <label for="comment">comment:</label>
            <textarea
              class="input"
              name="comment"
              id="comment"
              cols="30"
              rows="7"
              required
            ></textarea>
          </div>
        </div>
      </div>
    </article>
  </section>
</template>

<script>
export default {
  name: "Main",
};
</script>

<style lang="scss" scoped>
.post__inner {
  width: 90%;
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  line-height: 22px;
  font-size: 12px;
  margin: 50px 0 75px 0;
}
.post__immage {
  width: 100%;
}
.post__title {
  font-size: 18px;
  background-color: #ffffff;
  display: flex;
  padding: 20px 15px;
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
  align-items: center;
}
.post__title::before {
  content: "";
  background-image: url(../../assets/icons/heart.svg);
  background-size: cover;
  width: 22px;
  height: 22px;
  display: block;
  margin: 0 10px 0 0;
}
.post__data {
  display: flex;
  margin: 10px 15px;
  font-size: 11px;
  font-weight: bold;
  align-items: center;
}
.post__data * {
  color: #635f44;
}
.post__time {
  color: #7a7a7a;
}
.hashtag {
  display: flex;
}
.post__text {
  padding: 15px;
  background-color: #ffffff;
}
.post__socials {
  margin: 10px 0 0 0;
  color: #3b5997;
  display: flex;
  justify-content: space-between;
  border-top: 2px solid #ebeae3;
  border-bottom: 2px solid #ebeae3;
}
.post__social-wrapper {
  display: flex;
}
.post__social {
  display: block;
  background-size: cover;
  width: 22px;
  height: 22px;
}
.post__social:nth-child(1) {
  background-image: url(../../assets/icons/facebook.svg);
}
.post__social:nth-child(2) {
  background-image: url(../../assets/icons/twitter.svg);
}
.comment-wrapper {
  margin: 75px 0 0 0;
}
.comment__inner {
  padding: 0 0 0 25px;
}
.comment {
  display: flex;
}
.comment__paragraph {
  padding: 15px;
  background-color: #ffffff;
}
.comment__img {
  width: 50px;
  height: 50px;
  background-size: cover;
}
.comment__data {
  font-weight: bold;
  font-family: "Trebuchet MS";
  font-size: 11px;
  line-height: 48px;
  color: #cccabd;
}
.comment__from {
  color: #827e63;
}
.title2 {
  font-size: 16px;
  line-height: 20px;
  color: #737269;
  font-family: "Ardleys Hand";
  font-weight: bold;
  text-align: right;
}
.comment__title {
  margin: 0 60px 0 0;
}
.title2::after {
  content: " thoughts";
  margin: 0 -45px 0 0;
}
.form {
  padding: 20px;
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}
.form__item:nth-child(1) {
  height: 40px;
}
.form__item:nth-child(2) {
  margin: 20px 0;
  height: 40px;
}
.comment__form {
  margin: 10px 0 0 0;
  background-color: #ebeae4;
}
.form__item {
  display: grid;
  grid-template-columns: 1fr 5fr;
  background-color: #f2f1eb;
  text-align: center;
  line-height: 40px;
  color: #737269;
}
.input {
  border-left: 2px solid #737269;
}
</style>
