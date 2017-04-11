<template>
   <div class="swiper-container">
        <div class="swiper-wrapper">
            <div class="swiper-slide">
               <img src="http://img.wanyx.com/upload/picture/image/20131211/20131211110356_90032.jpg" alt="">
            </div>
            <div class="swiper-slide">
                <img src="http://www.005.tv/uploads/allimg/170324/204932AD-0.jpg" alt="">
            </div>
            <div class="swiper-slide">
                <img src="http://android.tgbus.com/download/uploadfiles_2115/201205/20120521102143342.jpg" alt="">
            </div>
            <div class="swiper-slide">
                <img src="http://img2.niutuku.com/desk/1208/1510/ntk-1510-24060.jpg" alt="">
            </div>
            <div class="swiper-slide">
                <img src="http://file.mumayi.com/forum/201505/06/130921u1aikza8h2iaifie.jpg" alt="">
            </div>
            <div class="swiper-slide">
                <img src="http://pic1.win4000.com/wallpaper/f/58b124b825676.jpg" alt="">
            </div>
            
            <div class="swiper-slide">
                <img src="http://img2.niutuku.com/desk/1207/1005/ntk122712.jpg" alt="">
            </div>
        </div>
        <div class="swiper-pagination"></div>
    </div>
</template>

<script>
import '../assets/lib/js/swiper.js'
export default {
  data () {
    return {
     
    }
  },
  mounted() {
       var mySwiper = new Swiper ('.swiper-container', {
         loop: true,
         autoplay : 2000,
        // 如果需要分页器
        pagination: '.swiper-pagination',
      })        
    }
}
</script>

<style>
    .swiper-container {
        width: 100%;
    }
    .swiper-slide {
       
    }
    .swiper-slide img{
        width:100%;
    }
    .swiper-pagination-bullet{
        background:green !important;
    }
    .swiper-pagination-bullet-active{
       background:red !important;
    }
</style>
