<template>
  <div class="App">
    <div class="xin">
      <div class="box">
        <div class="num">{{ num }}</div>
        <button class="jia" @click="jia">+</button>
        <button class="jian" @click="jian">-</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0
    }
  },
  methods: {
    jia() {
      this.num++
      console.log(this.num)
    },
    jian() {
      this.num--
      console.log(this.num)
    }
  },
  updated() {
    let num = this.$el.querySelector('.box .num')
    num.innerHtml = this.num
    console.log(this.num)
  }
}
</script>

<style lang="less" scoped>
.App {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  .xin {
    margin: 0 auto;
    width: 100vw;
    .box {
      margin-left: 40vw;
      .num {
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 2vw;
        margin-left: 5vw;
        width: 6vw;
        height: 3vw;
        background-color: aquamarine;
        border-radius: 10%;
      }
      .jia {
        margin-right: 10vw;
        width: 3vw;
        height: 2vw;
        background-color: aqua;
        border-radius: 10%;
      }

      .jian {
        width: 3vw;
        height: 2vw;
        background-color: aqua;
        border-radius: 10%;
      }
    }
  }
}
</style>
