<template>
  <Layout>
    <el-card class="card" v-for="item in 5" :key="item">
      <div slot="header" class="clearfix">
        <span>动态</span>
        <el-button style="float: right; padding: 3px 0" type="text">
          <i class="el-icon-share"></i>
        </el-button>
      </div>
      <div>新发布了github-pages页面</div>
    </el-card>
  </Layout>
</template>

<script>
export default {
  name: "move",
};
</script>

<style lang="scss" scoped>
.card {
  margin-bottom: 10px;
}
</style>