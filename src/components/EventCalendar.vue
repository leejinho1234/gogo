<template>
  <v-row class="fill-height">
    <v-col align="center">
      <v-sheet height="64">
        <v-toolbar flat color="white">
          <v-btn outlined class="mr-4" color="grey darken-2" @click="setToday">
            Today
          </v-btn>
          <v-btn fab text small color="grey darken-2" @click="prev">
            <v-icon small>mdi-chevron-left</v-icon>
          </v-btn>
          <v-btn fab text small color="grey darken-2" @click="next">
            <v-icon small>mdi-chevron-right</v-icon>
          </v-btn>
          <v-spacer></v-spacer>
          <v-menu bottom right>
            <template v-slot:activator="{ on }">
              <v-btn outlined color="grey darken-2" v-on="on" @click="test1">
                <span>{{ title }}</span>
              </v-btn>
            </template>
            <v-list>
              <v-list-item @click="selectYear = 2010" @change="test2">
                <v-list-item-title>2010</v-list-item-title>
              </v-list-item>
              <v-list-item @click="selectYear = 2020"  @change="test2">
                <v-list-item-title>2020</v-list-item-title>
              </v-list-item>
              <v-list-item @click="selectYear = 2021"  @change="test2">
                <v-list-item-title>2021</v-list-item-title>
              </v-list-item>
              <v-list-item @click="selectYear = 2022" @change="test2">
                <v-list-item-title>2022</v-list-item-title>
              </v-list-item>
            </v-list>
          </v-menu>
        </v-toolbar>
      </v-sheet>
      <v-sheet height="600" width="1300">
        <v-calendar
          ref="calendar"
          v-model="focus"
          color="primary"
          :events="events"
          :event-color="getEventColor"
          :now="today"
          :type="type"
          @click:event="showEvent"
          @change="updateRange"
        ></v-calendar>
      </v-sheet>
    </v-col>
  </v-row>
</template>

<script>
  export default {
    data: () => ({
      focus: '', //뭔지 모르겠음 
      type: 'month', //컨트롤 인터페이스에 캘린더 형식임
      start: null,
      end: null,
      selectedEvent: {},
      selectedElement: null,
      selectedOpen: false,
      events: [],
      colors: ['blue', 'indigo', 'deep-purple', 'cyan', 'green', 'orange', 'grey darken-1'],
      names: ['Meeting', 'Holiday', 'PTO', 'Travel', 'Event', 'Birthday', 'Conference', 'Party'],
      today: null, //사용하는 부분 지웠는데도 없다고 에러떠서 그냥 널처리
      selectYear: null, 
    }),
    computed: {
      title () {
        const { start, end } = this
        if (!start || !end) {
          return ''
        }

        const startMonth = this.monthFormatter(start)
        // console.log(startMonth); //title에 보이는 시작월임
        const endMonth = this.monthFormatter(end)
        // console.log(endMonth); //title에 보이는 끝나는 월임
        const suffixMonth = startMonth === endMonth ? '' : endMonth
        // console.log(suffixMonth); //title에 보이는 월은 항상 같음 주간, 일당 단위로 스케줄을 보면 필요하겠지만 지금은 필요없음으로 추정

        const startYear = start.year
        // console.log(startYear);
        const endYear = end.year
        // console.log(endYear);
        const suffixYear = startYear === endYear ? '' : endYear
        // console.log(suffixYear);

        const startDay = start.day + this.nth(start.day)
        // console.log(startDay); //title에 보이는 시작일자
        const endDay = end.day + this.nth(end.day)
        // console.log(endDay); //title에 보이는 마지막일자

        //type에 따라 변하는 시작일자와 끝일자로 title를 포맷해서 컴포넌트로 리턴
        // switch (this.type) {
        //   case 'month':
        //     return  startYear+"년 " + startMonth
        //   case 'week':
        //   case '4day':
        //     return `${startMonth} ${startDay} ${startYear} - ${suffixMonth} ${endDay} ${suffixYear}`
        //   case 'day':
        //     return `${startMonth} ${startDay} ${startYear}`
        // }
        
        //type은 일정하게 갈꺼니까 switch없이 바로 리턴
        return startYear+"년 " + startMonth
      },
      monthFormatter () {
        return this.$refs.calendar.getFormatter({
          timeZone: 'UTC', month: 'long',
        })
      },
    },
    mounted () {
      this.$refs.calendar.checkChange()
    },
    methods: {
      test1 () {
        //여러가지 date포맷 방식이 있지만
        //밑에 처럼 Date()함수로 셋팅하면 됨 월 일, 년도 시간 순
        const date1 = new Date('12 17, 1995 03:24:00');
      },
      test2 () {
        this.$refs.calendar.move((this.selectYear - this.start.year) * 12) 
          
      },
      getEventColor (event) {
        return event.color
      },
      //Today버튼을 클릭하면 실행
      //this.focus를 현재 날짜로 변경합니다.
      setToday () {
        this.focus = this.today
      },
      //title의 월을 이전 달로 이동
      prev () {
        //calendar의 내장함수를 호출합니다.
        this.$refs.calendar.prev()
      },
      //title의 월을 다음 달로 이동
      next () {
        //calendar의 내장함수를 호출합니다.
        this.$refs.calendar.next()
      },
      //달력에 이벤트를 클릭하면 실행
      showEvent ({ nativeEvent, event }) {
        alert("행사 url연결!!");
      },
      //달력의 이벤트를 셋팅합니다.
      //여기서 start, end는 data에 start와 end와는 다른 녀석들임
      //여기서 start, end는 calendar에서의 start와 end임
      updateRange ({ start, end }) {
        //이벤트들을 배열에 넣어줄거임 순서는 상관없고
        //나중에 start end에 있는 년도와 월로 db에서 가져오고 순서 상관없이 넣어 줄거임
        //db필요 컬럼은 name, start날짜, end날짜, 넣어줄 색상 정도임
        const events = []
        const min = new Date(`${start.date}T00:00:00`)
        const max = new Date(`${end.date}T23:59:59`)
        const days = (max.getTime() - min.getTime()) / 86400000
        const eventCount = this.rnd(days, days + 20)
        
        for (let i = 0; i < eventCount; i++) {
          const allDay = this.rnd(0, 3) === 0
          const firstTimestamp = this.rnd(min.getTime(), max.getTime())
          const first = new Date(firstTimestamp - (firstTimestamp % 900000))
          const secondTimestamp = this.rnd(2, allDay ? 288 : 8) * 900000
          const second = new Date(first.getTime() + secondTimestamp)

          events.push({
            name: this.names[this.rnd(0, this.names.length - 1)],
            start: this.formatDate(first, !allDay),
            end: this.formatDate(second, !allDay),
            color: this.colors[this.rnd(0, this.colors.length - 1)],
          })
        }

        this.start = start
        this.end = end
        this.events = events 
      },
      //쓸일이 없어염
      nth (d) {
        return d > 3 && d < 21
          ? 'th'
          : ['th', 'st', 'nd', 'rd', 'th', 'th', 'th', 'th', 'th', 'th'][d % 10]
      },
      //일수를 램덤으로 만들어 주는 함수인데 이건 db연결하면서 db에 맞게 변경해야함
      rnd (a, b) {
        return Math.floor((b - a + 1) * Math.random()) + a
      },
      //a은 Date()형식이고, withTime은 일수임
      //이벤트를 랜덤으로 만들어줄때 데이터셋에 쓰는건데 db연결하면서 쓸지여부를 생각해야하는 부분임
      formatDate (a, withTime) {
        return withTime
          ? `${a.getFullYear()}-${a.getMonth() + 1}-${a.getDate()} ${a.getHours()}:${a.getMinutes()}`
          : `${a.getFullYear()}-${a.getMonth() + 1}-${a.getDate()}`
      },
    },
  }
</script>