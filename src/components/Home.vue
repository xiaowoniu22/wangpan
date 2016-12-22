<template>
    <div>
       <div class="doc-filter-wrap">
           <div class="filter-item" data-filter="myfile" @click="showList">
               <img class="icon-filter" src="../assets/images/personal.png" />
               我的文件
           </div>
           <div class="filter-item" data-filter="share">
               <img class="icon-filter" src="../assets/images/share.png" />
               收到的共享
           </div>
           <div class="filter-item" data-filter="company">
               <img class="icon-filter" src="../assets/images/company.png" />
               公司文件
           </div>
           <div class="filter-divide">筛选器</div>
           <div class="filter-item" data-filter="favorite">
               <img class="icon-filter" src="../assets/images/star.png" />
               星标文件
           </div>
           <div class="filter-item" data-filter="myshare">
               <img class="icon-filter" src="../assets/images/myshare.png" />
               我的共享文件夹
           </div>
       </div>
       <div class="doc-list-wrap"></div>
       <div class="opt-wrap">
          <div class="opt-item action-newfolder" data-action="newfolder">
              <img src="../assets/images/newfolder.png" />
              <p>新建文件夹</p>
          </div>
          <div class="opt-item action-shareto" data-action="shareto">
              <img src="../assets/images/shareto.png" />
              <p>共享</p>
          </div>
          <div class="opt-item action-share" data-action="link">
              <img src="../assets/images/link.png" />
              <p>分享</p>
          </div>
          <div class="opt-item" data-action="send">
              <img src="../assets/images/send.png" />
              <p>发送</p>
          </div>
       </div>
    </div>
</template>
<style>
    .doc-filter-wrap {
        position: absolute;
        top: 0.88rem;
        bottom: 0;
        left: 0;
        right: 0;
        overflow-x: hidden;
        overflow-y: auto;
    }
    .doc-filter-wrap .filter-item {
        border-bottom: 1px solid #efefef;
        height: 0.5rem;
        line-height: 0.5rem;
        color: #000;
        font-size: 0.125rem;
        cursor: pointer;
    }

    .filter-item .icon-filter {
        width: 0.2rem;
        height: auto;
        margin-left: 0.2rem;
        margin-right: 20px;
        vertical-align: middle;
    }

    .doc-filter-wrap .filter-divide {
        height: 0.25rem;
        background-color: #efeff1;
        padding-left: 0.11rem;
        color: #a8a8a8;
        line-height: 0.26rem;
        border-bottom: 1px solid #d2d2d2;
        font-size: 0.12rem;
    }

    .opt-wrap {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 53px;
        background-color: #f8f8f8;
        border-top: 1px solid #b2b2b2;
        display: none;
    }
    .show-opt .opt-wrap {
        display: block;
    }

    .opt-wrap .opt-item {
        float: left;
        width: 25%;
        text-align: center;
        cursor: pointer;
    }

    .opt-wrap .opt-item.disabled {
        opacity: 0.5;
    }

    .opt-wrap .opt-item img {
        width: 18px;
        height: 18px;
        margin-top: 10px;
    }

    .opt-wrap .opt-item p {
        margin-top: 0px;
        color: #666;
        font-size: 12px;
    }

</style>
<script>
import Vue from 'vue'

new Vue({
  el: '.doc-filter-wrap',
  methods: {
    showList: function (event) {
      alert('hello')
    }
  }
})
</script>
