<template>
  <div class="red lighten-3 pa-3">
    <h3>오징어 대왕 프로필 상세 확인</h3>
    <p>이름: {{ nameOfChild }}</p>
    <p>나이: {{ ageOfChild }}</p>
    {{ sayHello }}
    <v-btn @click="switchSquidKing" elevation="2">대왕변경</v-btn>
    <div>
      프로필<br>
      {{ jobOfChild }}
    </div>
  </div>
</template>

<script>
  export default {
    // props: ['nameOfChild', 'ageOfChild', 'jobOfChild'],
    props: {
      nameOfChild: {
        type: String,
        required: true,
        default: '꼴뚜기'
      },
      ageOfChild: Number,
      jobOfChild: Object
    },
    computed: {
      sayHello() {
        return this.nameOfChild + '님이 올해의 대왕오징어입니다!';
      }
    },
    methods: {
      switchSquidKing() {
        this.nameOfChild = '구라라';
      }
    }
  }
</script>