<template lang="html">
  <Panel title="理财精选" :class="$style.panel">
    <section :class="$style.content">
      <dl :class="$style.item" v-for="item in items" :key="item.title">
        <dt>{{ item.title }}&nbsp;<span :class="item.sub ? $style.red : ''">{{ item.sub }}</span></dt>
        <dd>{{ item.rate }}</dd>
        <dd>{{ item.text }}</dd>
      </dl>
    </section>
  </Panel>
</template>

<script>
  import Panel from "../core/panel.vue"
  export default {
    components: {
      Panel
    },
    data() {
      return {
        items: [{
          title: "长乐盈",
          sub: "180天可质押",
          rate: "5.8%",
          text: "近1年历史年化投资回报率"
        },
        {
          title: "京智0号",
          sub: "大数据赋能",
          rate: "6.0%",
          text: "近1月历史年化投资回报率"
        },
        {
          title: "建信养老飞益鑫",
          sub: "",
          rate: "4.57%",
          text: "近7日年化收益"
        },
        {
          title: "小白基金",
          sub: "超短期",
          rate: "4.5%",
          text: "近7日年化收益"
        }]
      }
    }
  }
</script>

<style lang="scss" module>
  @import '../../css/element.scss';
  .panel {
    @include panel;
    .content {
      @include flex(row);
      justify-content: space-around;
      box-sizing: border-box;
      &:after{
        content: " ";
        display: block;
        width: 100%;
        height: 0px;
        box-sizing: border-box;
        border-bottom: 1px solid #ddd;
        position: relative;
        top: -208px;
      }
      .item {
        position: relative;
        width: 50%;
        box-sizing: border-box;
        &:after {
          content: " ";
          width: 1px;
          height: 136px;
          dispaly: block; 
          position: absolute;
          top: 50%;
          right: 0;
          margin-top: -60px;
          border-right: 1px solid #eee;
        }
        &:nth-child(2n) {
          &:after {
            display: none;
          }
        }
        padding: 34px 16px;
        dt {
          font-size: 30px;
          font-weight: 700;
          line-height: 42px;
          coor: #333;
          .red {
            font-size: 22px;
            color: #ff5155;
            border: 1px solid #ff5155;
            padding: 0 8px;
            vertical-align: 1px;
            margin-left: 2px;
          }
        }
        dd {
          &:nth-child(2){
            font-weight: 700;
            font-size: 44px;
            height: 58px;
            line-height: 58px;
            color: #FF5155;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
          &:nth-child(3){
            font-size: 24px;
            height: 34px;
            line-height: 34px;
            color: #999;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
        }
      }
    }
  }
</style>
