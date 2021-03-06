<template>
  <section class="main">
    <article class="post main__post">
      <div class="post__inner">
        <PostItem :post="post" :commentsCount="comments.length"></PostItem>
        <div class="comment-wrapper">
          <Comment
            v-for="comment of comments"
            :key="comment.id"
            :comment="comment"
          ></Comment>
        </div>
        <h2 class="title2 comment__title">post your<br /></h2>
        <Form></Form>
      </div>
    </article>
  </section>
</template>

<script>
import PostItem from "@/components/Main/PostItem/PostItem.vue";
import Comment from "@/components/Main/Comment/Comment.vue";
import Form from "@/components/Main/Form/Form.vue";

export default {
  name: "Main",
  components: {
    PostItem,
    Comment,
    Form,
  },
  data() {
    return {
      comments: [
        {
          id: 0,
          text: `Lorem ipsum, dolor sit amet consectetur adipisicing elit. Commodi,
            deleniti. Consectetur repellat quisquam molestias ipsum illo sit
            voluptatibus enim porro! Enim odio eos pariatur explicabo tenetur
            dolores sapiente? Quidem in nulla qua erat maxime animi! Assumenda sint
            nesciunt atque expedita quos porro eius cum repudiandae libero beatae
            nemo amet, excepturi adipisci aspernatur quasi voluptas dolore, est
            magnam at. At, fuga distinctio ipsa praesentium dolores necessitatibus
            quibusdam delectus harum facilis, alias similique sint quas corporis
            fugit id explicabo, repudiandae laborum temporibus odit?`,
          time: new Date(2011, 11, 15, 2, 3, 4),
          person: "Lucy",
        },
        {
          id: 1,
          text: `Lorem ipsum, dolor sit amet consectetur adipisicing elit.
            Commodi, deleniti. Consectetur repellat quisquam molestias ipsum
            illo sit voluptatibus enim porro! Enim odio eos pariatur
            explicabo tenetur dolores sapiente? Quidem in nulla quaerat
            maxime animi!`,
          time: new Date(2011, 11, 16, 6, 8, 14),
          person: "Jake",
        },
      ],
      post: {
        title: "Party people on the image above!",
        likesCount: "14",
        time: new Date(2011, 11, 16, 22, 10, 48),
        hashtags: ["Dance", "Party", "People"],
        text: `Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quis impedit
        tenetur veritatis magni, mollitia ipsa obcaecati alias? Dolorum officia
        corporis vitae, praesentium, sequi quam excepturi nisi voluptatum
        aperiam porro, repellat ut non deleniti obcaecati perspiciatis iure
        pariatur illum maiores ullam sunt nobis. Molestiae, pariatur nihil
        voluptate tenetur odio repellat mollitia dolorem, maiores itaque
        deserunt libero culpa aliquid commodi facere saepe vero assumenda
        deleniti soluta vitae a temporibus aut necessitatibus. Soluta possimus
        minus facere excepturi placeat sint eaque error. Magnam ab rem, vitae
        sit similique nisi laudantium, suscipit, reprehenderit repellat
        provident minus! Quaerat nisi error explicabo dolorum quae aliquid
        doloremque facilis.
        <br /><br />
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae, libero.
        Suscipit magnam omnis beatae id ipsam nam ipsa asperiores porro
        voluptatibus soluta tempora exercitationem explicabo nostrum sequi, ut
        voluptates illo.`,
        immage: "Image",
      },
    };
  },
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
.comment {
  &-wrapper {
    margin: 75px 0 0 0;
  }
  &__title {
    margin: 0 60px 0 0;
  }
}

.title2 {
  font-size: 16px;
  line-height: 20px;
  color: #737269;
  font-family: "Ardleys Hand";
  font-weight: bold;
  text-align: right;
  &::after {
    content: " thoughts";
    margin: 0 -45px 0 0;
  }
}
</style>
