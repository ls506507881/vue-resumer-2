<template>
  <div id="Editor">
        <nav>
          <ol>
            <li v-for="i in [0,1,2,3,4,5]" v-bind:class="{active:currentTab === i}" v-on:click="currentTab = i">
              <svg class="icon"><use v-bind:xlink:href="`#icon-${icons[i]}`"></use></svg>
            </li>
          </ol>
        </nav>
        <ol class="panes">
            <li v-bind:class="{active:currentTab ===0}">tab1</li>
            <li v-bind:class="{active:currentTab ===1}">tab2</li>
            <li v-bind:class="{active:currentTab ===2}">tab3</li>
            <li v-bind:class="{active:currentTab ===3}">tab4</li>
            <li v-bind:class="{active:currentTab ===4}">tab5</li>
            <li v-bind:class="{active:currentTab ===5}">tab6</li>
        </ol>
  </div>
</template>

<script>
export default {
  data(){
    return {
      currentTab:0,
      icons:['credentials_icon','bangong','jiaoyu','xiangmu','jiangbei','lianxi'],
    }
  }
}
</script>

<style lang="scss">
#Editor{
  display: flex;
  > nav{
    background: #000;
    width: 80px;
  > ol > li{
    text-align: center;
    padding: 16px 0;
    > .icon{
      width: 24px;
      height: 24px;
      color: #fff;
      }
    &.active{
        background:#fff;
        .icon{
          color: #000;
        }
    }
    }
    
  }
  > .panes{
    flex: 1;
    > li{
      display: none;
      &.active{
      display: block;
    }
    }
    
  }
  
}
</style>