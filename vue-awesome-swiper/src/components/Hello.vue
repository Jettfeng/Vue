<template>  
    <div>  
        <swiper :options="swiperOption"  ref="mySwiper">  
            <!-- 这部分放你要渲染的那些内容 -->  
            <swiper-slide v-for="(item,$index) in slideList" :key="$index">  
                <img :src="item.image" alt="">
            </swiper-slide>  
            <!-- 这是轮播的小圆点 -->  
            <div class="swiper-pagination" slot="pagination"></div>  
        </swiper>  
        <div class="footer"></div>
    </div>  
</template>  
<script>  
    import { swiper, swiperSlide } from 'vue-awesome-swiper'  
    export default {  
        components: {  
            swiper,  
            swiperSlide  
        },  
        data() {  
            return { 
                slideList: [
                  {
                    "clickUrl": "#",
                    "desc": "初夏",
                    image: "http://pic.qiantucdn.com/images/slideshow/58e6691e30fd3.jpg"
                  },
                  {
                    "clickUrl": "#",
                    "desc": "水墨世界",
                    image: "http://pic.qiantucdn.com/images/slideshow/58e11a5c00964.jpg"
                  },
                  {
                    "clickUrl": "#",
                    "desc": "油菜花",
                    image: "http://pic.qiantucdn.com/images/slideshow/58e44e7307494.png"
                  }
                ],
                swiperOption: {  
                pagination: '.swiper-pagination',  
                slidesPerView: 'auto',  
                centeredSlides: true,  
                paginationClickable: true,  
                spaceBetween: 0,  
                autoplay : 5000,
                    onSlideChangeEnd: swiper => {  
                        //这个位置放swiper的回调方法  
                        this.page = swiper.realIndex+1;  
                        this.index = swiper.realIndex;  
                    },  
                },  
                swiperSlides: [1, 2, 3, 4, 5]  
            }  
        },  
        //定义这个sweiper对象  
        computed: {  
  
            swiper() {  
              return this.$refs.mySwiper.swiper;  
            }  
        }
        // mounted () {  
        //     //这边就可以使用swiper这个对象去使用swiper官网中的那些方法  
        //     this.swiper.slideTo(0, 0, false);  
        // }  
  
    }  
</script>  
<style> 
*{
  margin: 0;
  padding: 0;
} 
.swiper-container{
  width: 100%;
}
.swiper-wrapper{
  width: 100%;
}
.swiper-slide{
  width: 100%;
  /*background: red;*/
}
.swiper-slide img{
  width: 100%;
}
.swiper-container-horizontal > .swiper-pagination-bullets{
  bottom: 0 !important;
}
.footer{
  width: 100%;
  height: 30px;
  background: green;
}
</style>