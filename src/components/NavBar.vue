<template>
  <nav>
    <ul>
      <NavBarItem v-for="item in items" :key="item" :item="item" />
    </ul>
  </nav>
</template>

<script>
import NavBarItem from "./NavBarItems";

export default {
  name: "NavBar",
  components: {
    NavBarItem,
  },
  props: {
    items: Array,
  },
};
</script>
