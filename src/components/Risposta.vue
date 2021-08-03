<template>
  <div>
    <button @click="chooseAnswer" class="answ_item">{{answ}}</button>
  </div>
</template>

<script>
export default {
  name: "Risposta",
  props: {
    answ: {
      type: String,
      
    }
  },
  methods: {
    chooseAnswer: function() {
      this.$emit('choose-answer');
    }

    
  }
}
</script>

<style lang="scss" scoped>
  

    .answ_item {
      background-color: transparent;
      border: none;
      position: relative;
      color: #fff;
      padding: 10px 20px;
      width: 200px;
      border: 1px solid #fff;
      cursor: pointer;

    }

    .answ_item:hover {
      background-color: #fff;
      color: black;
    }
    
  
</style>
