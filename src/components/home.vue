<template>
  <div class="hello">
    <article>
      <div class="blue color_div"></div>
      <div class="green color_div"></div>
    </article>
  </div>
</template>

<script>
import animationJs from 'animejs'
export default {
  data () {
    return {
      myAnimation: ''
    }
  },
  mounted () {
    this.myAnimation = animationJs({
      targets: ['.blue', '.green'],
      translateX: document.querySelector('.hello article').clientWidth / 2,
      rotate: 90,
      borderRadius: 10,
      duration: 2000,
      loop: true
    })
  }
}
</script>

<style scoped lang="less">
  .hello{
    width: 100%;
    height: 100%;
    position: absolute;
    article{
      padding: 20px 0;
      .color_div{
        width: 50px;
        height: 50px;
        padding: 10px 0;
      }
      .blue{
        background: deepskyblue;
      }
      .green{
        background: deeppink;
      }
    }
  }
</style>
