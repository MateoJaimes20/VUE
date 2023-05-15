<script setup>

</script>

<template>

  <div class="wrapper">
    <svg id="icon" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
      <path stroke-linecap="round" stroke-linejoin="round" d="M17.982 18.725A7.488 7.488 0 0012 15.75a7.488 7.488 0 00-5.982 2.975m11.963 0a9 9 0 10-11.963 0m11.963 0A8.966 8.966 0 0112 21a8.966 8.966 0 01-5.982-2.275M15 9.75a3 3 0 11-6 0 3 3 0 016 0z" />
    </svg>
  
    <div id="globito">
      3
    </div>

    <br>

    <spam class="buttom">+</spam>
    <spam class="buttom">-</spam>

    
  </div>
</template>

<style scoped>
.wrapper{
  display: inline-block;
  position: relative;
}

#globito{
  background-color:red;
  width: 24px;
  height: 24px;
  font-weight: bold;
  text-align: center;
  border-radius: 100%;
  position: absolute;
  top: -12px;
  right: -12px;
}

#icon{
  width: 100px;
  height: 100px;
}

.buttom{
  margin: 4px;
  color: white;
  width: 35px;
  height: 35px;
  text-align: center;
  border-radius: 6px;
  background-color: gray;
  display:inline-block;
}

.buttom:hover{
  background-color: green;
  cursor: pointer;
}
</style>
