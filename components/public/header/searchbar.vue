<template>
  <div class="search-panel">
    <el-row class="m-header-searchbar">
      <el-col :span="3" class="left">
        <img
          src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/logo.png"
          alt="美团">
      </el-col>
      <el-col :span="15" class="center">
        <div class="wrapper">
          <el-input v-model="searchValue" placeholder="搜索商家或地点" @focus="getFocus" @blur="loseBlur" @change="search"></el-input>
          <button class="el-button el-button--primary"><i class="el-icon-search"/></button>
          <dl class="hotPlace" v-if="isFocus && !searchValue">
            <dt>热门搜索</dt>
            <dd v-for="(item,index) of hotPlace" :key="index">{{item}}</dd>
          </dl>
          <dl class="searchList" v-if="isFocus && searchValue">
            <dd v-for="(item,index) of searchList" :key="index">{{item}}</dd>
          </dl>
        </div>
        <p class="suggset">
          <a href="#">故宫博物院</a>
          <a href="#">故宫博物院</a>
          <a href="#">故宫博物院</a>
          <a href="#">故宫博物院</a>
          <a href="#">故宫博物院</a>
        </p>
        <ul class="nav">
          <li>
            <nuxt-link to="/takeout" class="takeout">美团外卖</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/movie" class="takeout">猫眼电影</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/hotel" class="takeout">美团酒店</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/apartment" class="takeout">民宿/公寓</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/business" class="takeout">商家入驻</nuxt-link>
          </li>
        </ul>
      </el-col>
      <el-col :span="6" class="right">
        <ul class="security">
          <li><i class="refund"/>
            <p class="txt">随时退</p></li>
          <li><i class="single"/>
            <p class="txt">不满意免单</p></li>
          <li><i class="overdue"/>
            <p class="txt">随时退</p></li>
        </ul>
      </el-col>
    </el-row>
  </div>
</template>

<script>
  export default {
    name: "searchbar",
    data() {
      return {
        isFocus: false,
        searchValue: '',
        hotPlace: ['火锅','火锅','火锅','火锅','火锅'],
        searchList: ['烧烤','故宫']
      }
    },
    methods: {
      getFocus() {
        this.isFocus = true
      },
      loseBlur() {
        let self = this;
        setTimeout(function () {
          self.isFocus = false;
        },200)
      },
      search() {
        console.info(this)
        setTimeout(function () {

        },200)
      }
    }
  }
</script>

<style scoped>

</style>
