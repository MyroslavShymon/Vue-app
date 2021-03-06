<template>
  <main class="main-wrapper">
    <div class="main-page-inner main-inner">
      <Main></Main>
      <aside class="aside">
        <div class="aside__inner">
          <div class="aside__posts-small aside__item">
            <h2 class="aside__title">Totaly Random</h2>
            <div class="aside__content-wrapper">
              <div class="post-small">
                <h3 class="post-small__title">6 · Keep trying.</h3>
                <div class="post-small__inner">
                  <img
                    src="../assets/images/image_post-small-1.png"
                    alt=""
                    class="post-small__img"
                  />
                  <p class="post-small__paragraph">
                    Lorem Ipsum is simply dummy text of the printing and type
                    settin industry. Lorem Ipsum
                  </p>
                </div>
              </div>
              <div class="post-small">
                <h3 class="post-small__title">18 · The butterfly effect.</h3>
                <div class="post-small__inner">
                  <img
                    src="../assets/images/image_post-small-2.png"
                    alt=""
                    class="post-small__img"
                  />
                  <p class="post-small__paragraph">
                    Lorem Ipsum is simply dummy text of the printing and
                    typesettin industry. Lorem Ipsum
                  </p>
                </div>
              </div>
              <div class="post-small">
                <h3 class="post-small__title">
                  8 · Quit smoking, start drinking?
                </h3>
                <div class="post-small__inner">
                  <img
                    src="../assets/images/image_post-small-3.png"
                    alt=""
                    class="post-small__img"
                  />
                  <p class="post-small__paragraph">
                    Lorem Ipsum is simply dummy text of the printing and type
                    settin industry. Lorem Ipsum
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="aside__photos aside__item">
            <div class="aside__title">Latest photo</div>
            <div class="photos-wrapper aside__content-wrapper">
              <img
                src="../assets/images/recent1.png"
                alt=""
                class="photo-recenr"
              />
              <img
                src="../assets/images/recent2.png"
                alt=""
                class="photo-recenr"
              />
              <img
                src="../assets/images/recent3.png"
                alt=""
                class="photo-recenr"
              />
            </div>
            <a href="" class="more-photos">more photos</a>
          </div>
          <div class="aside__coments-small aside__item">
            <div class="aside__title">Recent Comments</div>
            <div class="aside__content-wrapper comments-small-wrapper">
              <div class="comment-small">
                <img
                  src="@/assets/images/avatars/Jake.png"
                  alt=""
                  class="comment-small__img"
                />
                <span class="comment-small__text">
                  Lorem Ipsum is simply dummy text of the printing and
                  typesettin industry. Lorem Ipsum has been the industry's
                  standart...</span
                >
              </div>
              <div class="comment-small">
                <img
                  src="../assets/images/avatars/Lucy.png"
                  alt=""
                  class="comment-small__img"
                />
                <span class="comment-small__text">
                  Lorem Ipsum is simply dummy text of the printing and
                  typesettin industry. Lorem Ipsum has been!</span
                >
              </div>
              <div class="comment-small">
                <img
                  src="../assets/images/avatars/Jake.png"
                  alt=""
                  class="comment-small__img"
                />
                <span class="comment-small__text"
                  >Lorem Ipsum is simply dummy text of the printing and
                  typesettin industry. Lorem Ipsum has been the industry's
                  standart and lep economica</span
                >
              </div>
            </div>
          </div>
        </div>
      </aside>
    </div>
  </main>
</template>

<script>
// @ is an alias to /src
import Main from "@/components/Main/Main.vue";

export default {
  name: "Home",
  components: {
    Main,
  },
};
</script>

<style lang="scss" scoped>
.main-wrapper {
  background-color: #f3f2ec;
}
.main-inner {
  margin: 10px auto;
  width: 100%;
  display: grid;
  grid-template-columns: 2fr 1fr;
}

.aside {
  background-color: #eae9e2;
}
.aside__item {
  padding: 0 10px 15px 10px;
}
.aside__content-wrapper {
  margin: 25px 0 0 0;
}
.aside__inner {
  margin: 50px 0 75px 0;
  font-size: 14px;
}
.aside__title {
  line-height: 20px;
  color: #3d3e3d;
  font-family: "Daniel";
  display: flex;
  align-items: center;
}
.aside__title::after {
  content: "";
  display: block;
  flex-grow: 1;
  height: 2px;
  background: rgb(234, 233, 226);
  background: linear-gradient(
    275deg,
    rgba(234, 233, 226, 1) 0%,
    rgba(209, 208, 202, 1) 100%
  );
  margin: 0 0 0 5px;
}
.post-small__title {
  display: flex;
  align-items: center;
}
.post-small__title::before {
  content: "";
  background-image: url(../assets/icons/heart_2.svg);
  background-size: cover;
  width: 22px;
  height: 22px;
  display: block;
  margin: 0 10px 0 0;
}
.post-small {
  margin: 10px 0;
  background-color: #fff;
  padding: 10px;
}
.post-small__inner {
  display: flex;
  align-items: center;
  padding: 10px 0 0 0;
  border-top: 2px solid #e9e8e1;
  margin: 10px 0 0 0;
}
.post-small__paragraph {
  padding: 0 0 0 10px;
  font-size: 12px;
  line-height: 20px;
  color: #787878;
  font-family: "Verdana";
}
.aside__photos {
  display: flex;
  flex-direction: column;
}
.photos-wrapper {
  display: flex;
  justify-content: space-between;
}
.more-photos {
  margin: 20px 0 0 0;
  font-size: 12px;
  line-height: 20px;
  color: #6d6e76;
  font-family: "Lucida Grande";
  display: flex;
  align-self: end;
  align-items: center;
}
.more-photos::after {
  content: "";
  display: block;
  background-size: cover;
  background-image: url(../assets/icons/photo.svg);
  width: 20px;
  height: 20px;
  margin: 0 0 0 10px;
}
.comment-small {
  display: flex;
  padding: 10px;
  background-color: #f6f5ef;
  align-items: center;
  transition: 0.2s;
}
.comment-small:hover {
  background-color: #e8dcd3;
  transition: 0.2s;
}
.comment-small:nth-child(2) {
  margin: 20px 0;
}
.comment-small__text {
  margin: 0 0 0 15px;
}
</style>
