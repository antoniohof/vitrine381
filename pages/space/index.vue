<template>
  <v-container>
nada

  </v-container>
</template>

<script>
import moment from 'moment'

export default {
  head: {
    title: 'Space',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Space about...'
      }
    ],
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
    const exhibitions = await $content("exhibitions").fetch()
    console.log(exhibitions)
    return {
      exhibitions
    }
  },
  methods: {
    getFormattedDate (value) {
      return moment(String(value)).format('DD.MM.YY')
    }
  }
}
</script>

<style lang="sass" scoped>

</style>
