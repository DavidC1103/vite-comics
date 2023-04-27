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
  </footer>
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
}


</style>