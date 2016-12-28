<template>
<div id="app">
    <div class="layout">
      <div class="header-wrap">
        <div class="mod-header">
          <a class="back" data-path="">
            <img class="goback" src="./assets/images/new_back.png"/>
          </a>
          <div class="title">文件管理</div>
          <div class="upload">上传</div>
          <div class="send" data-action="send">
            <img src="./assets/images/new_send.png"/>
          </div>
        </div>
      </div>
      <div class="search-wrap">
        <img class="icon-search" src="./assets/images/search.png"/>
        <input name="search" class="search-input" />
      </div>
      <component v-bind:is="currentView" :currentView="currentView" @on-view-change="onViewChange"></component>
    </div>
</div>
</template>
<script>
import Home from './components/Home'
import List from './components/List'


export default {
  name: 'app',
  data () {
    return {
      currentView: 'Home'
    }
  },
  methods: {
    onViewChange(val){
      this.currentView = val;//④外层调用组件方注册变更方法，将组件内的数据变更，同步到组件外的数据状态中
    },
  },
  components: {
    Home,List
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 100%;
  margin: 0 auto;
  overflow: hidden;
  height: 100%;
  position: relative;
}
#tongbupan-gap {
  width: 100%;
  height: 10px;
  background-color: #00bbd1;
}
#tongbupan {
  width: 100%;
  margin: 0 auto;
  overflow: hidden;
  height: 100%;
  position: relative;
}

.mod-header {
  background-color: #00bbd1;
  height: 0.48rem;
  line-height: 0.48rem;
  position: relative;
  font-size: 0.154rem;
  border-top: 1px solid #b2b2b2;
}

.mod-header .back {
  text-decoration: none;
  display: inline-block;
  vertical-align: middle;
  width: 25%;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
.mod-header .back .goback{
    width: 0.154rem;
    height: 0.154rem;
    position: relative;
    top: 0.03rem;
    padding-left: 0.05rem;
}
.mod-header .title {
  display: inline-block;
  width: 50%;
  text-align: center;
  color: #fff;
  vertical-align: middle;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  font-size: 0.154rem;
}

.mod-header .upload {
  color: #fff;
  width: 25%;
  text-align: right;
  display: inline-block;
  vertical-align: middle;
  cursor: pointer;
}
.mod-header .send {
  color: #fff;
  height: 0.48rem;
  width: 25%;
  text-align: right;
  display: inline-block;
  vertical-align: middle;
  cursor: pointer;
}
.mod-header .send img{
  height: 0.18rem;
  width: 0.18rem;
  margin-right: 0.32rem;
}
.auth-wrap {
  height: 0.3rem;
  background-color: #efeff1;
  padding: 0.05rem;
  position: relative;
  border-bottom: 1px solid #EEEEEE;
}
.auth-wrap .auth-input{
  height: 0.3rem;
  border: 1px #DADADA solid;
  border-radius: 0.2rem;
  width: 100%;
  font-size: 0.15rem;
  padding-left: 0.3rem;
  -webkit-appearance: none;
}
.search-wrap {
  height: 0.3rem;
  background-color: #efeff1;
  padding: 0.05rem;
  position: relative;
  border-bottom: 1px solid #eeeeee;
  z-index: 2;
}

.search-wrap .icon-search {
  position: absolute;
  top: 0.12rem;
  left: 0.14rem;
  width: 0.15rem;
  height: 0.15rem;
}

.search-wrap .search-input {
  height: 0.3rem;
  border: 1px #dadada solid;
  border-radius: 0.05rem;
  width: 100%;
  font-size: 0.15rem;
  padding-left: 0.3rem;
  -webkit-appearance:none;
}















</style>
