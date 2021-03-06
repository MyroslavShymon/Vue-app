<template>
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
        rows="7"
        required
      ></textarea>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "./Form.scss";
</style>
