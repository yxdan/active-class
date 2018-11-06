<template>
  <div class='hello'>
    <h1>{{ msg }}</h1>
    <ul>
      <li v-for="(item,index) of list" :key="item.index" @click="addClass(index)" :class="{active:current==index}">
        {{index}}-{{item}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'tab切换动态改变颜色',
      current: 0,
      list: [
        '标签1',
        '标签2',
        '标签2'
      ]
    }
  },
  methods: {
    addClass (index) {
      console.log(28, index)
      this.current = index
    }
  }
}
</script>

<!-- Add 'scoped' attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
.active{
  color: #42b983;
}
</style>
