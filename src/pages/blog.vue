<template>
  <Layout>
    <el-card shadow="never" class="card">
      <div class="box-card">
        <div class="input">
          <el-input v-model="input" placeholder="请输入关键字"></el-input>
          <el-button type="primary" class="radius" round>
            <i class="el-icon-search"></i>
          </el-button>
          <el-button type="primary" class="radius" round>
            <i class="el-icon-share"></i>
          </el-button>
        </div>
        <div>
          <el-button type="primary" class="radius" round>
            <i class="el-icon-edit"></i>写博文
          </el-button>
        </div>
      </div>
    </el-card>
    <el-card class="card" shadow="hover" v-for="item in 4" :key="item">
      <div slot="header" class="clearfix">
        <span style="color: #1e6bb8;">
          <i class="el-icon-edit-outline" style="  margin-right: 10px;"></i>2018.5.19 更新
        </span>
        <el-button style="float: right; padding: 3px 0" type="text">
          <i class="el-icon-share"></i>
        </el-button>
      </div>
      <div v-for="o in 4" :key="o" class="text item">{{'列表内容 ' + o }}</div>
    </el-card>
  </Layout>
</template>

<script>
export default {
  name: "blog",
};
</script>

<style lang="scss" scoped>
.card {
  margin-bottom: 10px;
}

.box-card {
  display: flex;
  justify-content: space-between;
  .input {
    display: flex;
    align-content: center;
    .radius {
      border-radius: 50%;
      padding: 12px;
      border: 1px solid #dcdfe6;
    }
  }
}
</style>