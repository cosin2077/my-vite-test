<template>
  <div class="header">
    <ul class="header-container">
      <li v-for="(link,index) in linkList" :class="linkClass(link)" :key="index">
        <a :href="link.url" :alt="link.title">{{link.title}}</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'header',
  data() {
    return {
      linkList: [
        {
          title: '首页',
          url: '/'
        },
        {
          title: '关于',
          url: '/about'
        },
        {
          title: '价格',
          url: '/pricing'
        },
        {
          title: '演示',
          url: '/show'
        },
      ]
    }
  },
  methods: {
    linkClass(link){
      if(location.pathname == (link.url)){
        return 'focus'
      }
    }
  },
}
</script>

<style>
.header{
  height: 40px;
  line-height: 40px;
  width: 100%;
  background: transparent;
  position: absolute;
  top: 0px;
  left: 0px;
  transition: all .5s;
}
.header:hover{
  box-shadow: 0px 2px 3px grey;
}

.header-container{
  list-style: none;
  display: flex;
  margin: auto;
  justify-content: flex-end;
  font-size: 1.2rem;
  padding-left: 30px;
  padding-right: 30px;
}
.header-container li{
  margin-left: 30px;
}
.header-container li.focus a{
  color: black;
}
.header-container li a{
  text-decoration: none;
  color: white;
  transition: all 0.5s ease-in-out;
}
.header-container li a:hover{
  color: black;
}
</style>