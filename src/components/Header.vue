<script>
import menuTop from '../js/menuTop.js';

    export default {
        name :'Header',
        data(){
            return{
                menuTop,
            }
        }
    
    }
</script>

<template>
    <header class="header-menu">
        <div class="dc-container">
            <img src="../assets/img/dc-logo.png" alt="">
            <div>
                <ul>
                    <li 
                     v-for="(menu, index) in menuTop"
                    :key="index">
                        <a href="">{{ menu.text }}</a>
                    </li>
                </ul>
            </div>
        </div>

    </header>
</template>


<style lang="scss">
@use'../scss/general.scss' as *;
@import '../scss/color.scss' ;
@import'../scss/variables.scss';

   header{
    background-color:white;
    height: 115px;
    margin-top: 40px;
    display: flex;
    align-items: center;
        img{
        width: 70px;
        };
   }
</style>