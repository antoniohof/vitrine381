<template>
  <div class='exhibition'>
    <h1>{{ exhibition.title }}</h1>
    <nuxt-content :document="exhibition" />
  </div>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  computed: {
  },
  components: {
  },
  async asyncData({ $content, params, error }) {
    let exhibition;
    try {
      exhibition = await $content("exhibitions", params.slug).fetch();
      // OR const article = await $content(`articles/${params.slug}`).fetch()
    } catch (e) {
      error({ message: "exhibition not found" });
    }
    return {
      exhibition,
    };
  },
  methods: {

  }
}
</script>

<style lang="sass" scoped>
.exhibition
  width: 100%

</style>
