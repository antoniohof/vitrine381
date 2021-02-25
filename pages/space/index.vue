<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>
        <!--Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.-->
        </h1>
        <div class='space_image'/>
        <p>
       <!-- Nam liber tempor cum soluta nobis eleifend option congue nihil imperdiet doming id quod mazim placerat facer possim assum. Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut aliquip ex ea commodo consequat.-->
        </p>
      <v-img
        class='space_image_2'
        lazy-src="/img/IMG_9321.JPG"
        max-width="80%"
        src="/img/IMG_9321.JPG"
      ></v-img>
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
  font-size: 16px
.space_image
  width: 100%
  height: 300px
  background-image: url('/img/IMG_2371_jpg.jpg')
  background-size: cover
  background-position-y: -131px
  width: 80%
  margin: 0 auto
  height: 250px
  margin-top: 50px
  margin-bottom: 50px

  @media only screen and (max-width: 600px)
    background-position-y: -73px

.space_image_2
  margin: 0 auto



p
  color: $font-color
  font-size: 14px
</style>
