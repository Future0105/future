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
    width: 100%;
    .box {
      margin-left: 40%;
      .num {
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 16px;
        margin-left: 9%;
        width: 100px;
        height: 30px;
        background-color: aquamarine;
        border-radius: 10%;
      }
      .jia {
        margin-right: 16%;
        width: 50px;
        height: 20px;
        background-color: aqua;
        border-radius: 10%;
      }

      .jian {
        width: 50px;
        height: 20px;
        background-color: aqua;
        border-radius: 10%;
      }
    }
  }
}
</style>
