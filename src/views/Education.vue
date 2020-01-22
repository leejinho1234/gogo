<template>
  <v-container fluid style="padding:0px">
    <v-layout frow wrap>
      <v-flex  align="center">
        <v-img src="https://ifh.cc/g/I3TY4.jpg"
          max-height="400" min-height="400">
          <br><br><br><br><br><br><br><br>
            <v-card-text align="center" id="title">교육</v-card-text>
            <v-card-text align="center" id="subTitle">반 려 견 과  반 려 인 의  행 복 한  동 행 을  위 해  교 육 강 의 와  우 수 한  교 육  시 설 을  소 개 해  드 립 니 다.</v-card-text>
        </v-img>
      </v-flex>
    </v-layout>
    <v-tabs grow centered id="tabs" dark >
      <v-tab id="tab" v-for="tabs in tab" :key="tabs.title" :to="tabs.to">{{ tabs.title }}</v-tab>
    </v-tabs>
    <br><br><br><br>
    <v-spacer></v-spacer>
    <v-card align="center" flat>
      <v-img src="https://ifh.cc/g/9ksel.png"
            max-width="300"
            min-width="300"></v-img>
    </v-card>
    <br><br><br><br>
    <v-layout row wrap>
      <v-flex xs12 sm6 md4 offset-md2>
        <v-col offset-md="0" cols="auto">
        <v-card>
          <iframe height="400" width="100%" src="https://www.youtube.com/embed/VZF0ST0-5vc?list=PLVh3TM0B0WtksY4ZQVNdD0aTG1Qm1mQNM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          <v-card-title primary-title>
            <div>
              <div class="headline">골든 리트리버</div>
              <span class="grey--text">gg</span>
            </div>
          </v-card-title>

          <v-card-actions>
            <v-btn flat color="purple">더보기</v-btn>
          </v-card-actions>
        </v-card>
        </v-col>
      </v-flex>

      <v-flex xs12 sm6 md4>
        <v-col offset-md="0" cols="auto">
        <v-card>
          <iframe height="400" width="100%" src="https://www.youtube.com/embed/VZF0ST0-5vc?list=PLVh3TM0B0WtksY4ZQVNdD0aTG1Qm1mQNM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
          <v-card-title primary-title>
            <div>
              <div class="headline">골든 리트리버</div>
              <span class="grey--text">gg</span>
            </div>
          </v-card-title>

          <v-card-actions>
            <v-btn flat color="purple">더보기</v-btn>
          </v-card-actions>
        </v-card>
        </v-col>
      </v-flex>

    </v-layout>
  </v-container>
</template>
<script>
export default {
  data () {
    return {
      tab: [
        {
          title: '전체보기'
        },
        {
          title: '기본지식 배우기'
        },
        {
          title: '견종별 모아보기'
        },
        {
          title: '전문 교육 기관'
        }
      ]
    }
  }
}
</script>
<style>
#tab{
  /* background-color:azure; */
  color: white;
  border-right: 0.5px solid gray;
}
#title{
    color:white;
    font-size:40px;
  }
  #subTitle{
    color:white;
    font-size:15px;
  }
</style>
