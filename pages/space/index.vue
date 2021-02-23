<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>
          Stet clita kasd gubergren
        </h1>
        <p>
        At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.        </p>
      </v-col>
    </v-row>
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
        content: 'Space'
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
h1
  font-family: Ribosoma
  color: $font-color

</style>
