<template>
  <v-container class='exhibitions'>
    <div v-for="exhibition of sortedExhibitions" :key="exhibition.slug">
      <NuxtLink :to="{ name: 'exhibitions-slug', params: { slug: exhibition.slug } }">
        <div class='exhibitions_body'>
          <div v-if="exhibition.thumbnail" class='exhibitions_body_thumbnail'>
            <img :src='exhibition.thumbnail'/>
          </div>
          <div class='exhibitions_body_content'>
            <time class='exhibitions_body_content_date'>{{ getFormattedDate(exhibition.date) }}</time>
            <h1 class='exhibitions_body_content_title'>{{ exhibition.title }}</h1>
            <p class='exhibitions_body_content_description'>{{ exhibition.description }}</p>
          </div>
        </div>
      </NuxtLink>
    </div>
  </v-container>
</template>

<script>
import moment from 'moment'

export default {
  head: {
    title: 'Exhibitions',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content: 'Exhibitions'
      }
    ],
  },
  data () {
    return {
    }
  },
  computed: {
    sortedExhibitions () {
      this.exhibitions.sort( ( a, b) => {
          return new Date(b.date) - new Date(a.date);
      });
      return this.exhibitions;
    }
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
*
  text-decoration: none !important
  color: $font-color
.exhibitions_body
  margin-bottom: 100px
  display: flex
  flex-direction: row
  justify-content: space-around
  &_thumbnail
    width: 45%
    img
      width: 100%
    @media only screen and (max-width: 600px)
      width: 100%
  &_content
    margin-top: 5%
    display: flex
    flex-direction: column
    width: 45%
    &_date
      font-size: 15px
    &_title
      overflow-wrap: break-word
      margin-top: 15px
      line-height: 34px
      font-family: Ribosoma
      font-size: 25px
    &_description
      overflow-wrap: break-word
      margin-top: 15px
      color: $font-color
      font-size: 15px
    @media only screen and (max-width: 600px)
      width: 100%
  @media only screen and (max-width: 600px)
    flex-direction: column

</style>
