<template>
  <li>
    <a :href="item.link">{{ item.text }}</a>
  </li>
</template>

<script>
export default {
  props: {
    item: String,
    link: String,
  },
};
</script>