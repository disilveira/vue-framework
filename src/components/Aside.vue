<template>
  <div class="sidenav">
    <AsideItems v-for="item in asideMenus" :key="item" :aside="item" />
  </div>
</template>

<script>
import AsideItems from "./AsideItems";

export default {
  components: {
    AsideItems,
  },
  props: {
    asideMenus: Array,
  },
};
</script>
