<template>
  <div class='main'>
    <div class='main_top'>
      <div class='main_top_logo'> VITRINE </div>

    </div>
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
.main
  width: 100%
  height: fit-content
  display: flex
  &_top
    display: flex
    width: 100%
    height: 50px
    position: absolute
    flex-direction: row
    top: 0
    &_logo
      font-size: 30px
      font-family: Ribosoma Slanted


</style>
