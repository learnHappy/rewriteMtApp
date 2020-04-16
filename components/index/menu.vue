<template>
  <div class="m-menu">
    <dl class="nav" @mouseleave="mouseleave">
      <dt>全部分类</dt>
      <dd @mouseenter="mouseenter" v-for="(item,index) of menu" :key="index">
        <i :class="item.type"/>{{item.name}}<span class="arrow"/>
      </dd>
    </dl>
    <div class="detail" v-if="kind" @mouseenter="sover" @mouseleave="sout">
      <template v-for="(item,idx) of curdetail">
        <h4 :key="idx">{{item.title}}</h4>
        <span v-for="childItem of item.child" :key="childItem">{{childItem}}</span>
      </template>
    </div>
  </div>
</template>

<script>
  export default {
    name: "menu",
    data() {
      return {
        menu: [{
          type: 'food',
          name: '美食',
          child: [{title: '美食', child: ['代金券', '甜点', '火锅', '自助餐']}]
        }, {
          type: 'takeout',
          name: '外卖',
          child: [{title: '外卖', child: ['美团外卖']}]
        }],
        kind: ''
      }
    },
    computed: {
      curdetail: function () {
        debugger
        return this.menu.filter((item) => item.type === this.kind)[0].child
      }
    },
    methods: {
      mouseleave() {
        let self = this;
        self._timer = setTimeout(() => {
          self.kind = ''
        }, 150)
      },
      mouseenter(e) {
        this.kind = e.target.querySelector('i').className
      },
      sover() {
        clearTimeout(this._timer)
      },
      sout() {
        this.kind = ''
      }
    }
  }
</script>

<style>

</style>
