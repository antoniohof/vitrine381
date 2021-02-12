<template>
  <div>
    VITRINE
  </div>
</template>

<script>
export default {
  head () {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
    }
  },
  data () {
    return {
    }
  },
  computed: {
  },
  components: {
  },
  async asyncData({ $content }) {
    /*
    const posts = await $content("blog").fetch()

    return {
      posts
    }
    */
  },
  methods: {

  }
}
</script>

<style lang="sass" scoped>
@import '@/assets/variables.sass'

</style>
