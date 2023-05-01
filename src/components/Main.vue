<script>
import jsonCard from '../../json/dc-comics.json'
    export default{
        name:'Main',
        props:{
            img: String,
            title: String
        },
        data(){
            return{
                jsonCard

            }
        }
    
    }
</script>

<template>
    <main>
        
        <div class="jumbotron">
            <img src="../assets/img/jumbotron.jpg" alt="">
        </div>

        <div class="content">
            <div class="dc-container">
                <span class="series">Current series</span>

               <div class="card-container">
                   <div class="card"
                   v-for="(element, index) in jsonCard"
                    :key="index">
                       <div class="img-container">
                           <img :src="element.thumb" alt="">
                       </div>
                       <span>{{element.series}}</span>
                   </div>

                   <button type="button">Load More</button>
               </div> 
                
            </div>
        </div>


    </main>
  
</template>


<style lang="scss">
@import '../scss/color.scss';
@import '../scss/general.scss';
    .jumbotron{
    height: 400px;
    overflow: hidden;
    }

    .content{
    color: white;
    padding: 50px 0;
    position: relative;

    .card-container{
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        width: 100%;
        .card{
            width: calc(100%/6);
            padding: 0 15px;
            margin-bottom: 50px;
            .img-container{
              width: 100%;
              aspect-ratio: 2/3;
              margin-bottom: 10px;
              img{
                width: 100%;
                height: 100%;
                object-fit: cover;
              }
            }
            span{
              text-transform: uppercase;
              font-weight: bold;
            }
        }
    }
    

    .series{
      position: absolute;
      left: 280px;
      top: -20px;
      padding: 10px 25px;
      text-transform: uppercase;
      background-color: $primary-color;
      font-weight: bold;
    }

    
   

    button{
      padding: 10px 40px;
      background-color: $primary-color;
      color: white;
      border: 2px solid transparent;
      text-transform: uppercase;
      font-weight: bold;
      cursor: pointer;
      &:hover{
        background-color: white;
        color: $primary-color;
        border: 2px solid $primary-color;
      }
    }
  }


</style>