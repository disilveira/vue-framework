<template>
  <a :href="aside.link">{{aside.text}}</a>
</template>

<script>
export default {
  props: {
    aside: Object,
  },
};
</script>