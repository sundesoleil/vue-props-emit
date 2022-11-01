<template>
  <div class="yellow lighten-3 pa-3">
    <h3>오징어 대왕을 변경하자!</h3>
    <p></p>
    <v-text-field
    label="이름"
    v-model="squid.name"></v-text-field>
    <v-text-field
    label="나이"
    v-model="squid.age"></v-text-field>
    <v-btn @click="changeKing">수정고고</v-btn>
  </div>
</template>

<script>
  export default {
    props: ['name', 'age'],
    data() {
      return {
        squid: {}
      }
    },
    created() {
      this.squid.name = this.name;
      this.squid.age = this.age;
    },
    methods: {
      changeKing() {
        console.log(this.squid);
        this.$emit('child', this.squid);
      }
    }
  }
</script>