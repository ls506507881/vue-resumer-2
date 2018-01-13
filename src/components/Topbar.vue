<template>
  <div id="Topbar">
        <div class="logo">
            Resumer
        </div>
        <div class="actions">
            <el-button type="primary">登录</el-button>
            <el-button>注册</el-button>
        </div>
  </div>
</template>

<style lang="scss">
#Topbar{
    display: flex;
    justify-content:space-between;
    align-items: center;
    padding: 16px;
    .logo{
        font-size: 20px;
    }
}
</style>

