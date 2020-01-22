<template>
<v-container fluid>
  <v-layout>
    <v-flex xs12>
      <v-app>  
        <div>
          <EVCarouesl/>
        </div>
        <div>
          <EvCalendar/>
        </div>
      </v-app>
    </v-flex>
  </v-layout>
</v-container>
</template>

<script>
  import EvCalendar from '../components/EventCalendar';
  import EVCarouesl from '../components/EventCarouesl';

  export default {
    components: {
        EvCalendar,
        EVCarouesl,
    },
    mounted () {
      console.log(this.$vuetify.breakpoint)
    },

    // computed: {
    //   imageHeight () {
    //     switch (this.$vuetify.breakpoint.name) {
    //       case 'xs': return '220px'
    //       case 'sm': return '400px'
    //       case 'md': return '500px'
    //       case 'lg': return '600px'
    //       case 'xl': return '800px'
    //     }
    //   },
    // },
  }


</script>


