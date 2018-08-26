<template lang="html">
  <Panel title="赚钱轮播图" :class="$style.panel">
    <section :class="$style.content">
      <Slider :items="items" :cname="$style.slider"></Slider>  
    </section>
  </Panel>
</template>

<script>
  import Panel from "../core/panel.vue"
  import Slider from '../core/slider.vue'
  export default {
    components: {
      Panel,
      Slider
    },
    data() {
      return {
        items: [
          {
            href: "home",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t13744/11/2508939408/43213/58bfe502/5a421ff3N52d0a474.jpg?width=750&height=320"
          }, 
          {
            href: "home",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t16138/325/817844900/36681/5d874455/5a422029Ncd678ea3.jpg?width=750&height=320"
          }, 
          {
            href: "home",
            src: "//img12.360buyimg.com/jrpmobile/jfs/t13465/324/2563794460/43029/3ffca963/5a421f83Ne8089231.jpg?width=750&height=320"
          }
        ]
      }
    }
  }
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    >h4{
      display: none;
    }
    .content{
      .slider{
        margin-top: 120px;
        img{
          width: 100%;
        }
      }
    }
  }
</style>
