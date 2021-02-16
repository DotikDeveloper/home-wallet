<template>
  <ul class="sidenav app-sidenav">
    <li v-for="link in links" :key="link.url" :exact="link.exact">
      <router-link :to="link.url" class="waves-effect waves-orange pointer">{{
        link.title
      }}</router-link>
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      links: [
        { title: "Счет", url: "/" },
        { title: "История", url: "history" },
        { title: "Планирование", url: "planning" },
        { title: "Новая запись", url: "detail-record" },
        { title: "Категории", url: "/categories" }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.router-link-active {
  border-bottom: 2px solid #ffa726;
  background-color: rgba(255, 168, 38, 0.087);
}
</style>
