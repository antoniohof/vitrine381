<template>
  <div class='exhibitions'>
    exhibitions
    <ul>
      <li v-for="exhibition of exhibitions" :key="exhibition.slug">
        <NuxtLink :to="{ name: 'exhibitions-slug', params: { slug: exhibition.slug } }">
          <!--<img :src="article.img" />-->
          <div>
            <h2>{{ exhibition.title }}</h2>
            <p>{{ exhibition.description }}</p>
          </div>
        </NuxtLink>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
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

  }
}
</script>

<style lang="sass" scoped>
.exhibitions

</style>
