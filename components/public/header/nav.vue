<template>
  <div class="m-nav">
    <ul class="nav">
      <li class="list">
        <nuxt-link to="/my">我的美团</nuxt-link>
        <dl>
          <dd>
            <nuxt-link to="/order">我的订单</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/mite">我的收藏</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">抵用券</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">账户设置</nuxt-link>
          </dd>
        </dl>
      </li>
      <li>
        <nuxt-link to="/order">手机APP</nuxt-link>
      </li>
      <li class="list bd">
        <nuxt-link to="/center">商家中心</nuxt-link>
        <dl>
          <dd>
            <nuxt-link to="/userCenter">登录商家中心</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/mite">我想合作</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">免费手机开店</nuxt-link>
          </dd>
          <dd>
            <nuxt-link to="/order">商家申请开票</nuxt-link>
          </dd>
        </dl>
      </li>
      <li class="list site">
        <nuxt-link to="/site">网站导航</nuxt-link>
        <div class="subContainer">
          <dl class="hotel">
            <dt>酒店旅游</dt>
            <dd>国际机票</dd>
            <dd>外海风景</dd>
            <dd>外海风景</dd>
            <dd>外海风景</dd>
            <dd>外海风景</dd>
            <dd>外海风景</dd>
            <dd>外海风景</dd>
            <dd>海景酒店</dd>
            <dd>海景酒店</dd>
          </dl>
          <dl class="food">
            <dt>美食</dt>
            <dd>烧烤</dd>
            <dd>啤酒</dd>
            <dd>羊肉串</dd>
          </dl>
          <dl class="movie">
            <dt>电影</dt>
            <dd>战狼</dd>
            <dd>盗梦空间</dd>
            <dd>盗梦空间</dd>
            <dd>盗梦空间</dd>
            <dd>盗墓笔记</dd>
            <dd>盗墓笔记</dd>
          </dl>
          <dl class="app">
            <dt>手机应用</dt>
            <dd>
              <a href="#">
                <img
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app">
              </a>
            </dd>
            <dd>
              <a href="#">
                <img
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app">
              </a>
            </dd>
            <dd>
              <a href="#">
                <img
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app">
              </a>
            </dd>
            <dd>
              <a href="#">
                <img
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app">
              </a>
            </dd>
            <dd>
              <a href="#">
                <img
                  src="//s0.meituan.net/bs/fe-web-meituan/e5eeaef/img/appicons/meituan.png"
                  title="美团app"
                  alt="美团app">
              </a>
            </dd>
          </dl>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: "navbar"
  }
</script>

<style lang="scss">
  @import "@/assets/css/public/header/topbar.scss";
</style>
