<template>
  <v-app>
    <v-main class='body' flex flex-row align-center w-full>
      <v-row class='topfixed'>
        <NuxtLink class='logo' to="/">
          <div class='logo_first'>Vitrine</div>
          <div class='logo_second'>381</div>
        </NuxtLink>
        <div class='menu'>
          <menu class='menu_items'>
            <NuxtLink :class="{selected: $route.path === '/space'}" class='menu_items_item' to="/space">space</NuxtLink>
            <NuxtLink :class="{selected: $route.path === '/calls'}" class='menu_items_item' to="/calls">calls</NuxtLink>
            <NuxtLink :class="{selected: $route.path === '/exhibitions'}" class='menu_items_item' to="/exhibitions">exhibitions</NuxtLink>
            <NuxtLink :class="{selected: $route.path === '/contact'}" class='menu_items_item' to="/contact">contact</NuxtLink>
          </menu>
        </div>
      </v-row>
      <v-container class='maincontainer' fluid>
        <v-row align="center" class='maincontainer_wrapper'>
          <nuxt />
        </v-row>
      </v-container>
    </v-main>
    <div class='foreground'>
    </div>
  </v-app>
</template>

<script>
export default {
  head: {
    title: 'Home',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Home about...'
      }
    ],
  },
  mounted () {
    console.log('mounted vitrine app')
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="sass" scoped>
.foreground
  position: fixed
  z-index: 1000
  opacity: 0.10
  color: red
  pointer-events: none
  // background-image: url('/img/trasparent-texture.png')
  width: 100vw
  background-repeat: repeat
  height: 100vh
.body
  min-width: 50vw
  margin-left: 5%
  margin-right: 5%
  margin-top: 20px
  border: 1px solid $menu-color
  min-height: 250px
  margin-bottom: 20px

.logo
  cursor: pointer
  padding: 0px
  text-decoration: none
  font-size: 22px
  width: fit-content
  display: flex
  flex-direction: column
  margin-left: 35px
  margin-top: 20px
  color: $menu-color
  &_first
    font-family: Ribosoma AntiSlanted
  &_second
    margin-top: -10px
    font-family: Ribosoma Slanted


.topfixed
  justify-content: space-between
  display: flex
  flex-direction: row
  margin-bottom: 15px

.menu
  height: 100%
  width: 15%
  right: 0
  position: absolute
  border-left: 1px solid $menu-color
  min-width: 80px
  justify-content: center
  // background-image: url("/img/texture-menu.png")
  // background-size: auto 600px
  // background-color: black
  &_items
    display: flex
    flex-direction: column
    width: fit-content
    margin: 0 auto
    margin-top: 23px
    &_item
      min-width: 57px
      text-decoration: none
      color: $font-color
      cursor: pointer
      font-size: 12px
      font-family: 'PT Sans', sans-serif
      &:hover
        text-decoration: underline
      &.selected
        font-style: italic
        text-decoration: none !important
        font-weight: bold
  @media only screen and (max-width: 600px)
    width: 10%
    height: fit-content
    // border-bottom: 1px solid $menu-color
    border-left: none
    padding-bottom: 20px
.maincontainer
  padding-left: 0
  margin-right: 0
  margin-left: 0
  width: 100%
  padding-right: max(100px, 15%)
  &_wrapper
    max-width: max(600px, 70%)
    margin: 0 auto

  @media only screen and (max-width: 600px)
    padding-right: 0px
    padding-top: 25px



</style>