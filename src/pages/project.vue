<template>
  <Layout>
    <el-card class="card" shadow="hover" v-for="item in 4" :key="item">
      <div slot="header" class="clearfix">
        <span style="color: #1e6bb8;">
          <i class="el-icon-edit-outline" style="  margin-right: 10px;"></i>vue-dialog
        </span>
        <el-button style="float: right; padding: 3px 0" type="text">前往github</el-button>
      </div>
      <!-- <div v-for="o in 4" :key="o" class="text item">{{'列表内容 ' + o }}</div> -->
      <div>
        <div class="card">最近更新 2019-03-29 12:36:56</div>
        <div class="card">This is yet another vue dialog component.</div>
        <div class="footer">
          <div>
            <span class="right">
              <i class="el-icon-star-off"></i>
              0
            </span>
            <span class="right">
              <i class="el-icon-view"></i>
              0
            </span>
            <span>
              <i class="el-icon-bell"></i>
              0
            </span>
          </div>
          <div>
            <el-tag type="success">vue</el-tag>
          </div>
        </div>
      </div>
    </el-card>
  </Layout>
</template>

<script>
export default {
  name: "project",
};
</script>

<style lang="scss" scoped>
.right {
  margin-right: 10px;
}
.card {
  margin-bottom: 10px;
}
.footer {
  display: flex;
  justify-content: space-between;
}
</style>