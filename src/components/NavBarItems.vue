<template>
  <li>
    <a :href="item.link">{{ item.text }}</a>
  </li>
</template>

<script>
export default {
  name: "NavBarItems",
  props: {
    item: String
  },
};
</script>