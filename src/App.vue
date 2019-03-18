<template>
  <div id="app">
    <!-- 组件 -->
    <div class="chajian">
      <input type="button" value="+" @click="jia">
      <span>{{initnum}}</span>
      <input type="button" value="-" @click="jian">
    </div>
  </div>
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      initnum: 15,
      initmax: 30,
      initmin: 1,
      initbushu: 2
    };
  },
  methods: {
    jia() {
      this.initnum += this.initbushu;
      if (this.initnum > this.initmax) {
        this.initnum = this.initmax;
      }
    },
    jian() {
      this.initnum -= this.initbushu;
      if (this.initnum < this.initmin) {
        this.initnum = this.initmin;
      }
    }
  },
  components: {}
};
</script>

<style lang="scss">
.chajian {
  margin: 300px auto;
  width: 150px;
  height: 100%;
  input {
    width: 50px;
    height: 100%;
  }
  span {
    width: 50px;
    height: 100%;
    text-align: center;
    display: inline-block;
  }
}
</style>
