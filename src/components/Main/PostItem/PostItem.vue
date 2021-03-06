<template>
  <div class="post__item">
    <img
      :src="require(`@/assets/images/${post.immage}.png`)"
      alt=""
      class="post__immage"
    />
    <h2 class="post__title">{{ post.likesCount }} · {{ post.title }}</h2>
    <div class="post__data">
      <time
        :datetime="post.time"
        class="post__time"
        v-html="`${setTime}|`"
      ></time>
      <ul class="hashtag post__hashtegs">
        <li
          class="hashtag__item"
          v-for="(hashtag, hashtagIndex) of post.hashtags"
          :key="hashtagIndex"
        >
          <a href="hashtag__link" v-html="`&nbsp;${hashtag}&nbsp;`"></a>
        </li>
      </ul>
      <div
        class="post__comments-count"
        v-html="`|&nbsp;${commentsCount} Comments`"
      ></div>
    </div>
    <div class="post__text">
      <p v-html="post.text"></p>
      <div class="post__socials">
        Liked it? Share it!
        <div class="post__social-wrapper">
          <a href="" class="post__social"></a>
          <a href="" class="post__social"></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    post: Object,
    commentsCount: Number,
  },
  computed: {
    setTime() {
      const months = [
        "Jan",
        "Feb",
        "Mar",
        "Apr",
        "May",
        "Jun",
        "Jul",
        "Aug",
        "Sep",
        "Oct",
        "Nov",
        "Dec",
      ];

      function fullTime(time) {
        return time < 10 ? "0" + time : time;
      }
      return `${this.post.time.getDate()} ${
        months[this.post.time.getMonth()]
      }, ${this.post.time.getFullYear()} at ${fullTime(
        this.post.time.getHours()
      )}:${fullTime(this.post.time.getMinutes())}&nbsp;`;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./PostItem.scss";
</style>
