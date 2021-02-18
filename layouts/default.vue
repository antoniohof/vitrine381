<template>
  <v-app>
    <v-main class='body' flex flex-row align-center w-full>
      <v-layout class='topfixed' h-full>
        <div class='logo'>
          <div class='logo_first'>Vitrine</div>
          <div class='logo_second'>381</div>
        </div>
        <div class='menu'>
          <div class='menu_items'>
            <NuxtLink class='menu_items_item' to="/space">space</NuxtLink>
            <NuxtLink class='menu_items_item' to="/calls">calls</NuxtLink>
            <NuxtLink class='menu_items_item' to="/exhibitions">exhibitions</NuxtLink>
            <NuxtLink class='menu_items_item' to="/contact">contact</NuxtLink>
          </div>
        </div>
      </v-layout>
      <v-container fluid>
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
  max-height: calc(100vh - 100px)
  margin-left: 5%
  margin-right: 5%
  margin-top: 20px
  border: 1px solid rgba(80,80,80,0.5)
  min-height: 250px
.logo
  padding: 0px
  font-size: 22px
  width: fit-content
  display: flex
  flex-direction: column
  margin-left: 35px
  margin-top: 30px
  color: rgba(120,120,120,0.9)
  &_first
    font-family: Ribosoma AntiSlanted
  &_second
    margin-top: -10px
    font-family: Ribosoma Slanted


.topfixed
  justify-content: space-between
  display: flex
  flex-direction: row
  margin-bottom: 20px

.menu
  height: 100%
  width: 120px
  right: 0
  position: absolute
  border-left: 1px solid rgba(80,80,80,0.5)
  min-width: 100px
  justify-content: cente
  &_items
    display: flex
    flex-direction: column
    width: fit-content
    margin: 0 auto
    margin-top: 20px
    &_item
      text-decoration: none
      color: rgba(60,60,60,0.9)
      cursor: pointer
      font-family: 'PT Sans', sans-serif
      &:hover
        text-decoration: underline !important

.container
  width: calc(100% - 120px)
  margin: 0
</style>