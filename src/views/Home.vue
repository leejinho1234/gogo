<template>
<v-card flat>
  <v-carousel cycle hide-delimiters show-arrows>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >
    <v-layout align-center>
    <v-flex><div>{{ item.text }}</div></v-flex>
    </v-layout>
    </v-carousel-item>
  </v-carousel>
  <v-toolbar height="220" flat>
    <v-spacer></v-spacer>
    <v-img src="https://ifh.cc/g/L3Zw0.png"
          max-width="300"
          max-height="500"
           position="center"
    ></v-img>
    <v-spacer></v-spacer>
  </v-toolbar>
  <v-container>
    <v-row centered>
      <v-col offset-md="2" xs12 sm6 md6 lg3 xl3 cols="2">
          <v-img xs6 src="https://ifh.cc/g/O6Dtq.jpg"
              max-width="800"
              min-width="500"
              style="cursor:pointer"
        ></v-img>
      </v-col>
      <v-col offset-md="2" xs12 sm6 md6 lg3 xl3 cols="6">
          <v-img src="https://ifh.cc/g/6f4s0.gif"
              max-width="320"
              min-width="320"
              style="cursor:pointer;"
        ></v-img><br>
        <v-img src="https://ifh.cc/g/KoVIs.jpg"
        max-width="320"
        min-width="320"
        style="cursor:pointer;"
        ></v-img>
      </v-col>
    </v-row>
  </v-container>
    <!-- <v-row>
      <v-col offset-md="2" xs12 sm6 md6 lg3 xl3 cols="4">
        <v-img xs6 src="https://ifh.cc/g/O6Dtq.jpg"
        max-width="800"
        min-width="800"
        style="cursor:pointer"
        ></v-img>
      </v-col>
      <v-col offset-md="1" xs12 sm6 md6 lg3 xl3 cols="2">
        <v-img src="https://ifh.cc/g/6f4s0.gif"
        max-width="320"
        min-width="320"
        style="cursor:pointer;"
        ></v-img>
        <br>
        <v-img src="https://ifh.cc/g/KoVIs.jpg"
        max-width="320"
        min-width="320"
        style="cursor:pointer;"
        ></v-img>
      </v-col>
    </v-row> -->
</v-card>
</template>
<script>
export default {
  data () {
    return {
      items: [
        {
          src: 'https://ifh.cc/g/olWeL.jpg',
          text: 'gdgd'
        },
        {
          src: 'https://ifh.cc/g/3QMao.jpg',
          text: 'gdasdd'
        }
      ]
    }
  }
}
</script>
