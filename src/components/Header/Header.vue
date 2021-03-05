<template>
  <div>
    <header class="header">
      <div class="main-page-inner header__inner">
        <h1 class="logo-wrapper">
          <router-link to="/" class="logo">net stories</router-link>
        </h1>
        <nav class="nav-wrapper">
          <ul class="nav">
            <NavigationItem
              v-for="navigationItem of navigationItems"
              v-bind:key="navigationItem.id"
              v-bind:navigationTitle="navigationItem.text"
            ></NavigationItem>
          </ul>
        </nav>
      </div>
    </header>
    <router-view />
  </div>
</template>

<script>
import NavigationItem from "@/components/Header/NavigationItem/NavigationItem.vue";
export default {
  name: "Header",
  components: {
    NavigationItem,
  },
  data() {
    return {
      navigationItems: [
        { id: 0, text: "Home" },
        { id: 1, text: "Blog" },
        { id: 2, text: "Porfolio" },
        { id: 3, text: "Photos" },
        { id: 4, text: "Extras" },
        { id: 5, text: "Contact" },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
.main-page-inner {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 10px;
  height: 100%;
}
.header {
  background-color: #282c2a;
  position: sticky;
  top: 0;
  &__inner {
    width: 100%;
    display: grid;
    grid-template-columns: 2fr 1fr;
  }
}
.nav {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.logo {
  outline: 2px dashed #952b2b;
  outline-offset: -4px;
  height: 100%;
  display: inline-block;
  padding: 10px 15px;
  background: #c12727;
  font-size: 33px;
  color: #ffffff;
  font-family: "Daniel";
  text-align: center;
  text-shadow: 2px 3.464px 1.5px rgba(0, 0, 0, 0.4);
}
</style>
