<template>
  <div class="blue lighten-3 pa-3">
    <h1>오징어대왕은 누구?</h1>
    <h3>Who is the King Of Squid?</h3>
    <p>이름: {{ name }}</p>
    <v-btn elevataion="2" @click="changeSquidKing">오징어 대왕 변경</v-btn>
    <v-layout row wrap mt-3>
      <v-flex xs12 sm6>
        <SquidKingDetail :nameOfChild="name" :ageOfChild="age" :jobOfChild="profile"></SquidKingDetail>
      </v-flex>
      <v-flex xs12 sm6>
        <SquidKingChange 
        :name="name" 
        :age="age"
        @child="parents">
        </SquidKingChange>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import SquidKingDetail from "./SquidKingDetail.vue"
import SquidKingChange from "./SquidKingChange.vue"

export default {
  components: {
    SquidKingDetail,
    SquidKingChange
  },
  data() {
    return {
      name: '선',
      age: 123,
      profile: {
        hobby: '잠자기',
        specialty: '못생기기'
      }
    }
  },
  methods: {
    changeSquidKing() {
      this.name = "니니"
    },
    parents(squid) {
      this.name = squid.name;
      this.age = squid.age;
      console.log('내가 신호를 수신함ㅋ');

    }
  }
}
</script>