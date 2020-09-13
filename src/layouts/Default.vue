<template>
  <div class="layouts">
    <div class="nav">
      <div class="nav_content">
        <div class="title">tangpeng</div>
        <p>欢迎来到唐鹏的个人微博</p>
        <div>
          <el-button class="button">Github主页</el-button>
          <el-button class="button">微博源码</el-button>
        </div>
      </div>
    </div>
    <div class="body">
      <div class="header">
        <el-menu class="el-menu-demo" mode="horizontal">
          <el-submenu index="1">
            <template slot="title">了解博主</template>
            <el-menu-item index="2-1">github主页</el-menu-item>
            <el-menu-item index="2-2">其他博客</el-menu-item>
          </el-submenu>
          <el-submenu index="2">
            <template slot="title">其他网站</template>
            <el-menu-item index="2-1">v2ex</el-menu-item>
          </el-submenu>
        </el-menu>
        <div class="right_message">
          <div class="message">
            <span class="title">GitHub-tabgpeng</span>
            <div class="address">
              <i class="el-icon-location"></i> 温州
            </div>
          </div>
          <!-- el-icon-location -->
          <img src="../asstes/images/touxiang.jpeg" width="52px" height="52px" />
        </div>
      </div>
      <el-row class="content" :gutter="20">
        <el-col class="left" :span="5">
          <el-card class="box-card" shadow="never">
            <g-link
              class="slier_item"
              :to="slier.path"
              v-for="slier in slier_list"
              :key="slier.name"
            >
              <i :class="slier.icon"></i>
              {{slier.name}}
            </g-link>
          </el-card>
        </el-col>
        <el-col class="right" :span="19">
          <slot></slot>
        </el-col>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  name: "layout",
  data() {
    return {
      slier_list: [
        {
          name: "最新动态",
          icon: "el-icon-star-off",
          path: "/",
        },
        {
          name: "社交圈",
          icon: "el-icon-mobile-phone",
          path: "/social",
        },
        {
          name: "博客列表",
          icon: "el-icon-edit-outline",
          path: "/blog",
        },
        {
          name: "开源项目",
          icon: "el-icon-headset",
          path: "/project",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.nav {
  height: 400px;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
  background-image: linear-gradient(
    120deg,
    rgb(38, 144, 249),
    rgb(252, 45, 45)
  );
  color: rgba(255, 255, 255, 0.7);
  .nav_content {
    text-align: center;
    .title {
      font-size: 32px;
      font-weight: bold;
    }
    .button {
      padding: 0.75rem 1rem;
      display: inline-block;
      margin-bottom: 1rem;
      color: rgba(255, 255, 255, 0.7);
      background-color: rgba(255, 255, 255, 0.08);
      border-color: rgba(255, 255, 255, 0.2);
      border-style: solid;
      border-width: 1px;
      border-radius: 0.3rem;
      -webkit-transition: color 0.2s, background-color 0.2s, border-color 0.2s;
      transition: color 0.2s, background-color 0.2s, border-color 0.2s;
    }
  }
}
.body {
  max-width: 64rem;
  margin: -30px auto 0 auto;
  .header {
    display: flex;
    justify-content: space-between;
    // line-height: 61px;
    border: solid 1px #e6e6e6;
    background: #fff;
    border-radius: 3px;
    z-index: 2;
    padding-right: 30px;
    margin-bottom: 30px;
    // display: flex;
    // justify-content: center;
    .right_message {
      display: flex;
      align-items: center;
      // justify-content: center;
      .message {
        padding-right: 15px;
        color: rgb(96, 98, 102);
        .title {
          font-size: 20px;
          font-weight: bold;
        }
        .address {
          text-align: right;
        }
      }
    }
  }
  .content {
    .left {
      .slier_item {
        display: block;
        text-decoration: none;
        text-align: center;
        font-size: 14px;
        color: #303133;
        padding: 20px 0;
        cursor: pointer;
        &:hover {
          background-color: #ecf5ff;
        }
      }
    }
  }
}

ul.el-menu-demo.el-menu--horizontal.el-menu {
  border-bottom: none;
}
</style>
