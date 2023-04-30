<script>
import ctaList from '../../js/ctaList.js'
    export default{
        name: 'CTA',
        data(){
            return{
                ctaList
            }
        },
        methods:{
            getImage(img){
            return new URL(img, import.meta.url).href;
    }

        }
    }
</script>

<template>
    <div class="footer-top-cta">
        <div class="dc-container">
            <div class="elements" v-for="(element, index) in ctaList" :key="index">
                <img :src="getImage(`../../assets/img/${element.img}`)">
                <span>{{element.text}}</span>
            </div>
        </div>
    </div>
  
</template>


<style lang="scss">
@import '../../scss/general.scss';
@import '../../scss/color.scss';
@import'../../scss/variables.scss';

.footer-top-cta{
    background-color: $primary-color;
    padding: 50px;
    display: flex;
    vertical-align: middle;
    span{
        color: white;
        text-transform: uppercase;
        font-size:  15px ;
    }
    img{
        height: 55px;
        margin-right: 15px;
    }
    .elements{
        display: flex;
        align-items: center;
        &:last-child{
            img{
                height: 40px;

            }
        } 
    }
    
}
</style>