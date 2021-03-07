<template>
  <div class="comment">
    <img
      :src="require(`@/assets/images/avatars/${comment.person}.png`)"
      alt=""
      class="comment__img"
    />
    <div class="comment__inner">
      <p class="comment__paragraph">
        {{ comment.text }}
      </p>
      <div class="comment__data">
        posted on
        <time :datetime="comment.time">{{ setTime }}</time>
        <span class="comment__from">by {{ comment.person }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: { comment: Object },
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
      return `${this.comment.time.getDate()} ${
        months[this.comment.time.getMonth()]
      }, ${this.comment.time.getFullYear()} at ${fullTime(
        this.comment.time.getHours()
      )}:${fullTime(this.comment.time.getMinutes())} `;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "./Comment.scss";
</style>
