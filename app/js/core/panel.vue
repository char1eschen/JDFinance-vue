<template lang="html">
  <section :class="[panelClass, cname]">
    <h4>-&nbsp;{{ title }}&nbsp;-</h4>
    <slot/>
  </section>
</template>

<script>
  export default {
    props: {
      cname: {
        type: String,
        default: ""
      },
      title: {
        type: String,
        default: ""
      }
    },
    data() {
      return {
        panelClass: "panel"
      }
    }
  }
</script>

<style lang="scss">
  @import "../../css/element.scss";
  .panel {
    @include panel;
    h4 {
      font-weight: 700;
    }    
  }
</style>
