<template>
  <div class='main'>
    <div class='main_menu'>
      <div class='main_menu_items'>
        <NuxtLink class='main_menu_item' to="/space">space</NuxtLink>
        <NuxtLink class='main_menu_item' to="/calls">calls</NuxtLink>
        <NuxtLink class='main_menu_item' to="/exhibitions">exhibitions</NuxtLink>
        <NuxtLink class='main_menu_item' to="/contact">contact</NuxtLink>
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
  display: flex
  justify-content: flex-end
  margin-top: -99px
  height: calc(100% + 25px)
  &_menu
    border-left: 1px solid rgba(0,0,0,0.5)
    width: 200px
    height: 100%
    justify-content: center
    &_items
      display: flex
      flex-direction: column
      width: fit-content
      margin: 0 auto
      margin-top: 20px
    &_item
      text-decoration: none
      color: black
      margin-left: 20px
      cursor: pointer
      font-family: 'PT Sans', sans-serif
      &:hover
        text-decoration: underline !important

</style>
