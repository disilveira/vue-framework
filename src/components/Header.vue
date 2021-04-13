<template>
  <header>
    <h3>{{ title }}</h3>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {
    title: String,
  },
};
</script>
