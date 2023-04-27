
<script>
    export default {
        name :'Header',
        data(){
            return{
                
            }
        }
    
    }
</script>

<template>
    <header>
        <div class="dc-container">
            <img src="../assets/img/dc-logo.png" alt="">
            <div></div>
        </div>

    </header>
</template>


<style lang="scss">
@use'../scss/general.scss';

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