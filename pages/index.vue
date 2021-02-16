<template>
  <div class='main'>
    <div class='main_top'>
      <div class='main_top_logo'> VITRINE 381 </div>
      <div class='main_top_menu'>
        <div class='main_top_menu_item'>exhibitions</div>
        <div class='main_top_menu_separator'>/</div>
        <div class='main_top_menu_item'>space</div>
      </div>
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
  width: calc(100vw - 50px)
  height: calc(100vh - 50px)
  display: flex
  margin: 5px
  border-top: 1px solid black
  border-left: 1px solid black
  &_top
    display: flex
    width: 100%
    height: 50px
    position: absolute
    flex-direction: row
    top: 10px
    &_logo
      padding: 15px
      font-size: 22px
      width: 200px
      height: 100px
      font-family: Ribosoma Slanted
    &_menu
      width: 100%
      margin-right: 10%
      justify-content: flex-end
      display: flex
      align-self: center
      flex-direction: row
      &_separator
        margin-left: 10px
        pointer-events: none
      &_item
        margin-left: 10px
        cursor: pointer

</style>
