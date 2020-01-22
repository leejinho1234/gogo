<template>
  <v-container fluid style="padding-left:0px; padding-right:0px;" >
    <v-layout wrap>
      <v-flex>
        <v-img src="https://ifh.cc/g/BS5mM.jpg" max-height="400" min-height="400">
          <br><br><br><br><br><br><br><br>
            <v-card-text align="center" id="title">회사 소개</v-card-text>
            <v-card-text align="center" id="subTitle">반 려 견 과  반 려 인 을  위 한  "미 니 펫" 을  소 개 합 니 다 .</v-card-text>
      </v-img>
        <br><br>
        <v-col offset-md="3">
          <v-img src="https://ifh.cc/g/dHQj9.png"
            max-width="900"
            min-width="360"></v-img>
        </v-col>
        <br><br>
      </v-flex>
    </v-layout>
    <v-layout wrap>
      <v-flex>
      <v-row justify="center">
        <v-col offset-md="1" cols="auto">
          <v-card>
            <v-img src="https://ifh.cc/g/fbDp5.jpg"
                  max-width="700"
                  min-width="300"></v-img>
          </v-card>
        </v-col>
        <v-col>
          <v-card align="center" flat>
            <div class="v-card__text">
              <p class="num">01</p>
              <br>
              <p style="font-weight: bold; font-size:20px;">반려견과 반려인이 함께 하는 다양한 이벤트 소개</p>
              <br>
              <p>/</p>
              <br>
              <p>미니펫은 국내에 반려견과 반려인이 함께 참여 할 수 있는 다양한 이벤트를 소개해주는 업체 입니다.</p>
            </div>
          </v-card>
        </v-col>
      </v-row>
      </v-flex>
      <v-flex>
        <v-row>
          <v-col offset-md="1" cols="auto">
          <v-card>
            <v-img src="https://ifh.cc/g/581PC.jpg"
                  max-width="700"
                  min-width="300"></v-img>
          </v-card>
        </v-col>
        <v-col>
          <v-card align="center" flat>
            <div class="v-card__text">
              <p class="num">02</p>
              <br>
              <p style="font-weight: bold; font-size:20px;">반려견과 반려인이 함께 지낼 수 있게 교육 프로그램 소개</p>
              <br>
              <p>/</p>
              <br>
              <p>미니펫은 반려견과 반려인이 함께 지낼 수 있게 다양한 교육 프로그램을 소개 및 체험을 제공합니다.</p>
            </div>
          </v-card>
        </v-col>
        </v-row>
      </v-flex>
       <v-flex>
        <v-row>
          <v-col offset-md="1" cols="auto">
          <v-card>
            <v-img src="https://ifh.cc/g/T9mRk.jpg"
                  max-width="700"
                  min-width="300"></v-img>
          </v-card>
        </v-col>
        <v-col>
          <v-card align="center" flat>
            <div class="v-card__text">
              <p class="num">03</p>
              <br>
              <p style="font-weight: bold; font-size:20px;">잃어버린 반려견을 찾을수 있게 도와드립니다</p>
              <br>
              <p>/</p>
              <br>
              <p>미니펫은 잃어버린 반려견을 사람들과의 커뮤니케이션을 이용해 빠르고 안전하게 찾을 수 있게 도와드립니다.</p>
            </div>
          </v-card>
        </v-col>
        </v-row>
      </v-flex>
    </v-layout>
  </v-container>
</template>
<style>
  #title{
    color:white;
    font-size:40px;
  }
  #subTitle{
    color:white;
    font-size:15px;
  }
  .num{
    color:black;
    font-weight: bolder;
    font-size: 60px;
    color: #eea08b
  }
</style>
