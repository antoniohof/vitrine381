<template>
  <v-app>
    <v-main class='body'>
      <div class='logo'>
        <div class='logo_first'>Vitrine</div>
        <div class='logo_second'>381</div>
      </div>
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
  margin-left: 100px
  margin-right: 100px
  margin-top: 20px
  border: 1px solid rgba(0,0,0,0.5)
  min-height: 250px
.logo
  padding: 0px
  font-size: 22px
  width: fit-content
  display: flex
  flex-direction: column
  margin-left: 35px
  margin-top: 30px
  &_first
    font-family: Ribosoma AntiSlanted
  &_second
    margin-top: -10px
    font-family: Ribosoma Slanted

.container
  height: 100%
</style>