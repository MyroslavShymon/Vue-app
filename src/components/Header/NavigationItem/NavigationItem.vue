<template>
  <li class="nav__item">
    <router-link v-bind:to="navigationItemLink" class="nav__link">{{
      navigationTitle
    }}</router-link>
  </li>
</template>

<script>
export default {
  name: "NavigationItem",
  props: {
    navigationTitle: String,
  },
  computed: {
    navigationItemLink() {
      return this.navigationTitle == "Home"
        ? "/"
        : "/" + this.navigationTitle.toLowerCase();
    },
  },
};
</script>

<style lang="scss" scoped>
.nav__link {
  font-size: 13px;
  color: #898888;
  transition: 0.2s;
  &:hover {
    color: #b4b4b4;
    transition: 0.2s;
  }
}
</style>
