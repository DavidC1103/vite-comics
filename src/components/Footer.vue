<script>
import {dcComics, dc, sites, shop} from '../js/listFooter.js'
import FooterBottom from '../components/partials/FooterBottom.vue'
import cta from '../components/partials/cta.vue'


    export default{
        name :'Footer',
        components:{
          FooterBottom,
          cta
        },
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
    <cta />
  
    <div class="footer-middle">

      <div class="dc-container">
        <div class="footer-middle-menu">
  
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
    </div>
    <FooterBottom />
</footer>
</template>


<style lang="scss">
@use'../scss/general.scss' as *;
@import '../scss/color.scss';
@import'../scss/variables.scss';

.footer-middle{
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



</style>