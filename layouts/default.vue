<template>
  <v-app>
    <v-main class='body' flex flex-row align-center w-full>
      <v-layout class='topfixed' h-full>
        <NuxtLink class='logo' to="/">
          <div class='logo_first'>Vitrine</div>
          <div class='logo_second'>381</div>
        </NuxtLink>
        <div class='menu'>
          <div class='menu_items'>
            <NuxtLink :class="{selected: $route.path === '/space'}" class='menu_items_item' to="/space">space</NuxtLink>
            <NuxtLink :class="{selected: $route.path === '/calls'}" class='menu_items_item' to="/calls">calls</NuxtLink>
            <NuxtLink :class="{selected: $route.path === '/exhibitions'}" class='menu_items_item' to="/exhibitions">exhibitions</NuxtLink>
            <NuxtLink :class="{selected: $route.path === '/contact'}" class='menu_items_item' to="/contact">contact</NuxtLink>
          </div>
        </div>
      </v-layout>
      <v-container class='maincontainer' fluid>
        <nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
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
.body
  min-width: 50vw
  margin-left: 5%
  margin-right: 5%
  margin-top: 20px
  border: 1px solid $menu-color
  min-height: 250px
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
  min-width: 100px
  justify-content: cente
  &_items
    display: flex
    flex-direction: column
    width: fit-content
    margin: 0 auto
    margin-top: 25px
    &_item
      min-width: 57px
      text-decoration: none
      color: $menu-color
      cursor: pointer
      font-size: 12px
      font-family: 'PT Sans', sans-serif
      &:hover
        text-decoration: underline
      &.selected
        font-style: italic
        text-decoration: none !important
        font-weight: bold
.maincontainer
  padding-left: 0
  width: 100%
  margin-right: 0
  margin-left: 0
  padding-right: max(100px, 15%)
</style>