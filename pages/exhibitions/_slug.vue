<template>
  <v-container class='exhibition'>
    <h1 class='exhibition_title'>{{ exhibition.title }}</h1>
    <p class='exhibition_date'>{{ getFormattedDate(exhibition.date) }}</p>
    <nuxt-content class='exhibition_content' :document="exhibition" />
  </v-container>
</template>

<script>
import moment from 'moment'

export default {
  data () {
    return {
    }
  },
  computed: {
  },
  components: {
  },
  async asyncData({ $content, params, error }) {
    let exhibition;
    try {
      exhibition = await $content("exhibitions", params.slug).fetch();
      // OR const article = await $content(`articles/${params.slug}`).fetch()
    } catch (e) {
      error({ message: "exhibition not found" });
    }
    return {
      exhibition,
    };
  },
  methods: {
    getFormattedDate (value) {
      return moment(String(value)).format('DD.MM.YY')
    }
  }
}
</script>

<style lang="sass" scoped>
*
  color: $font-color

.exhibition
  width: 100%
  &_title
    font-family: Ribosoma
    font-size: 25px
    margin-bottom: 30px
  &_date
    font-size: 14px
</style>

<style lang="sass">
.exhibition_content
  width: 80%
  margin: 0 auto
  img
    width: 100% !important
    max-width: 100%
  p
    font-size: 14px


</style>