<template>
  <div>
    
    <header>
      <div class="container-logo">
        <img src="img/logo.png" alt="">
      </div>
    </header>
    
    
    <h2>{{color}}</h2>
  
  </div>

</template>

<script>

export default {
  name: "Contenitore",

  }
</script>

<style lang="scss" scoped>
  header {
    height: 400px;
    background: blue;

    .container-logo {
        height: 300px;
        width: 300px;
        margin: 40px auto;
        
      img {
        width: 100%;
      }
    }
  }
</style>
