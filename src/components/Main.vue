<template>
  <div>
      <main>
          <div class="container-lg">
              <div class="row">
                  <div class="col-12 ">
                      <div class="row">
                          <div class="col-12 d-flex flex-wrap">
                                <div class="card mx-auto d-block" v-for="(element,index) in brani" :key="index">
                                    <img class="card-img-top" :src="element.poster" alt="Card image cap">
                                    <div class="card-body">
                                        <h5 class="card-title text-light">{{element.title}}</h5>
                                        <h6 class="card-text text-light">{{element.author}}</h6>
                                        <p class="card-text text-light">{{element.year}}</p> 
                                    </div>
                                </div>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
      </main>
  </div>
</template>

<script>
    import axios from 'axios';
export default {
    data(){
        return{
            apiUrl : "https://flynn.boolean.careers/exercises/api/array/music",
            brani : [],

        }
    },
    created(){
        this.canzone()
    },
    methods :{
        canzone(){
            axios
            .get(this.apiUrl)  
            .then(picker =>{
                this.brani= picker.data.response;
                
            })
        }
    }

}
</script>
<style lang="scss" scoped>
main{
    background-color: #1E2D3B;
}
.card{
    background-color: #1E2D3B;
    margin: 20px auto;
    border: none;
    width: 14rem;
    img{
        width: 200px;
    }
    h5{
        font-size: 15px;
    }
    
    
    
}


</style>