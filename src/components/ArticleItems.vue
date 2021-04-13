<template>
  <section>
    <article>
      <h2>{{ article.title }}</h2>
      <p>
        {{ article.text }}
      </p>
    </article>
  </section>
</template>

<script>
export default {
  props: {
    article: Object,
  },
};
</script>