<template>
  <v-app>
    <v-main class='body'>
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
  width: calc(100vw - 50px)
  height: calc(100vh - 50px)
  display: flex
  margin: 20px
  border-top: 1px solid black
  border-left: 1px solid black
</style>