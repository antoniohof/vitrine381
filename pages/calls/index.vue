<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>
          Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis.
        </h1>
        <p>
          Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat. Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi.           </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import moment from 'moment'

export default {
  head: {
    title: 'Calls',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Calls'
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
