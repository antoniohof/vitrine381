<template>
  <div class='exhibition'>
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
