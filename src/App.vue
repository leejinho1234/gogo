<template>
 <v-card flat>
    <v-toolbar height="100" style="border-bottom: 1px solid #E3DFDE" flat>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <router-link to="/login">LOGIN</router-link>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-toolbar-title><img src="https://ifh.cc/g/ywJDY.png" width="200"></v-toolbar-title>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <router-link to="/join">JOIN</router-link>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
    <v-spacer></v-spacer>
  </v-toolbar>
  <v-toolbar flat style="border-bottom: 10px solid #E3DFDE" height="50">
    <v-tabs grow centered>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
      <v-tab v-for="bar in title" :key="bar.title" :to="bar.to">{{ bar.titleName }}</v-tab>
      <v-spacer></v-spacer>
      <v-spacer></v-spacer>
  </v-tabs>
  </v-toolbar>
    <router-view></router-view>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        title: [
          {
            titleName: 'ABOUT',
            to: '/about'
          },
          {
            titleName: 'EVENT',
            to: '/event'
          },
          {
            titleName: 'EDUCATION',
            to: '/education'
          },
          {
            titleName: 'HELP',
            to: '/help'
          },
          {
            titleName: 'Q&A'
          }
        ]
      }
    }
  }
</script>
