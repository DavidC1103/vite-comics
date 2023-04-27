<script>
import {dcComics, dc, sites, shop} from '../js/listFooter.js'

    export default {
        name :'FooterTop',
        data(){
            return{
              dcComics,
              dc, 
              sites, 
              shop
          }
        }
      }
</script>

<template>
  <footer>
    <div class="dc-container">
      <div class="footer-top-menu">

        <div class="dc-me">
          <div>
            <h4>DC COMICS</h4>
            <ul>
              <li
              v-for="(comics, index) in dcComics"
              :key="index">
                <a href="">{{ comics.text }}</a>
              </li>
            </ul>
          </div>

          <div class="dc-mt">

            <h4>SHOP</h4>
            <ul>
              <li
              v-for="(merch, index) in shop"
              :key="index">
                  <a href="">{{ merch.text }}</a>
              </li>
            </ul>
          </div>
        </div>

        <div class="dc-me">
          <h4>DC</h4>
          <ul>
            <li
            v-for="(dc, index) in dc"
            :key="index">
              <a href="">{{ dc.text }}</a>
            </li>
          </ul>
        </div>

        <div>
          <h4>SITES</h4>
          <ul>
            <li
              v-for="(site, index) in sites"
              :key="index">
                  <a href="">{{ site.text }}</a>
              </li>
          </ul>
        </div>

        
      </div>
    </div>
    <img src="../assets/img/dc-logo-bg.png" alt="">
  </footer>

  <div class="footer-bottom">
    <div class="dc-container">
      <button>SIGN-UP NOW!</button>
      <div class="follow-us-flex">

        <h4>FOLLOW US</h4>
        <img src="../assets/img/footer-facebook.png" alt="">
        <img src="../assets/img/footer-youtube.png" alt="">
        <img src="../assets/img/footer-twitter.png" alt="">
        <img src="../assets/img/footer-pinterest.png" alt="">
        <img src="../assets/img/footer-periscope.png" alt="">
        
        
      </div>
    </div>
    

  </div>
</template>


<style lang="scss">
@use'../scss/general.scss' as *;
@import '../scss/color.scss';
@import'../scss/variables.scss';

footer{
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat:no-repeat ;
    min-height: 350px;
    background-size: cover;
    display: flex;
    align-items: center;
    position: relative;
    overflow: hidden;
    img{
      position: absolute;
      right: 300px;
      
    }

  }
.footer-bottom{
  height: 120px;
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