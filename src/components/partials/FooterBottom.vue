<script>
    export default{
        name :'FooterBottom',
        data(){
          return{
           
          }
        }
    }
    
</script>

<template>
    <div class="footer-bottom">
        <div class="dc-container">
            <button>SIGN-UP NOW!</button>
            <div class="follow-us-flex">
                <h4>FOLLOW US</h4>
                <img src="../../assets/img/footer-facebook.png" alt="">
                <img src="../../assets/img/footer-youtube.png" alt="">
                <img src="../../assets/img/footer-twitter.png" alt="">
                <img src="../../assets/img/footer-pinterest.png" alt="">
                <img src="../../assets/img/footer-periscope.png" alt="">
            </div>
        </div>
    </div>
</template>


<style lang="scss" scoped>
@use'../../scss/general.scss' as *;
@import '../../scss/color.scss';
@import'../../scss/variables.scss';

.footer-bottom{
  padding: 30px;
  background-color: $quinary-color;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
      button{
        color: white;
        font-size: 17px;
        font-weight: bold;
        padding: 15px;
        border: 2px solid $primary-color;
        background-color: rgba(255, 255, 255, 0);
      }

      .follow-us-flex{
        display: flex;   
        align-items: center;
        h4{
          color: $primary-color;
          font-size: 20px;
          margin-right: 10px;
        }
        img{
          margin-left: 20px;
        }
      }
   
}

</style>