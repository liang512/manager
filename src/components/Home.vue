<template>
  <div class="basic-layout">
    <div class="nav-side"></div>
    <div class="content-right">
      <div class="nav-top">
        <div class="bread">面包屑</div>
        <div class="user">用户</div>
      </div>
      <div class="wrapper">
        <div class="main">
          <router-view style="height: 100%"></router-view>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Home"
}
</script>

<style scoped lang="scss">
.basic-layout {
  position: relative;

  .nav-side {
    position: fixed;
    width: 200px;
    height: 100vh;
    background-color: #001529;
    color: #ffffff;
    overflow-y: auto;
    transition: width .5s;
  }

  .content-right {
    margin-left: 200px;

    .nav-top {
      height: 50px;
      line-height: 50px;
      display: flex;
      justify-content: space-between;
      background-color: #fff;
      border-bottom: 1px solid #ddd;
      padding: 0 20px;
    }

    .wrapper {
      background-color: #eef0f3;
      padding: 20px;
      height: calc(100vh - 50px);

      .main {
        background-color: #fff;
        height: 100%;
      }
    }
  }
}

</style>