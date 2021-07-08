<template>
  <div> 
    <header>
    <div class="container-lg">
      <div class="row">
        <div class="col-12">
           <img src="@/img/logo.png" alt="">
        </div>
      </div>
    </div>
    </header>
  </div>
</template>

<script>
  
export default {
  name: 'Header',
}
</script>


<style scoped lang="scss">
header{
  height: 70px;
  background-color: black;
  img{
    height: 65px;
  }
}
</style>
