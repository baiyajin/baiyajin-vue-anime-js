<template>
  <div class="hello">
    <article>
      <div class="blue"></div>
      <div class="green"></div>
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
      translateX: '10rem',
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
    .blue{
      background: deepskyblue;
      width: 50px;
      height: 50px;
    }
    .green{
      background: deeppink;
      width: 50px;
      height: 50px;
    }
  }
</style>
