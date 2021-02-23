<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>
          Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis.
        </h1>
        <p>
          Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat.
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  head () {
    return {
      script: [{ src: 'https://identity.netlify.com/v1/netlify-identity-widget.js' }]
    }
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
    /*
    const posts = await $content("blog").fetch()

    return {
      posts
    }
    */
  },
  methods: {

  }
}
</script>

<style lang="sass" scoped>
h1
  font-family: Ribosoma
  color: $font-color
</style>
