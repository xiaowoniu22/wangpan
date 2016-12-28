<template>
<div>
  <div class="doc-list-wrap" style="display: block;" >
    <div class="doc-item" v-for="list in lists">
      <span class="checkbox "></span>
      <span class="filename ">{{list.name}}</span>
      <em class="ficon-pt "></em>
    </div>
  </div>
</div>
</template>
<script>
export default {
  data(){
    return {
        lists:[
          {name:"test.xls"},
          {name:"test1.xls"},
          {name:"test2.xls"},
          {name:"test3.xls"},
          {name:"test4.xls"},
          {name:"test5.xls"}
        ]

    }
  }
}
</script>
<style>
.doc-list-wrap {
    display: none;
    position: absolute;
    left: 0;
    right: 0;
    top: 0.88rem;
    bottom: 0;
    overflow-x: hidden;
    overflow-y: auto;
}

.show-opt .doc-list-wrap {
    bottom: 61px;
}
.doc-item {
    position: relative;
    border-bottom: 1px solid #efefef;
    height: 0.5rem;
    line-height: 0.5rem;
    cursor: pointer;
}

.doc-item .filename {
    position: absolute;
    left: 0.85rem;
    right: 0;
    white-space: nowrap;
    text-overflow: ellipsis;
    overflow: hidden;
    font-size: 0.125rem;
}

.doc-item .checkbox {
    display: inline-block;
    width: 0.4rem;
    height: 0.5rem;
    background: url(../assets/images/unchecked.png) no-repeat 0.15rem;
    vertical-align: middle;
}

.doc-item .checkbox.checked {
    background-image: url(../assets/images/checked.png);
}
</style>

