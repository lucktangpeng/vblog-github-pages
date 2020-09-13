<template>
  <Layout>
    <el-card class="box-card" shadow="never">
      <el-tabs v-model="activeName" type="card" @tab-click="handleClick">
        <el-tab-pane label="粉丝" name="first">
          <el-row class="user_body" :gutter="20">
            <el-col class="user_item" :span="8" v-for="item in 10" :key="item">
              <el-card shadow="never" class="card">
                <div>
                  <i class="el-icon-star-off"></i> lililiwj
                </div>
                <div>
                  <i class="el-icon-message"></i> TA的主页
                </div>
                <img src="https://avatars1.githubusercontent.com/u/38744589?v=4" width="100%" alt />
              </el-card>
            </el-col>
          </el-row>
        </el-tab-pane>
        <el-tab-pane label="关注" name="second">关注</el-tab-pane>
      </el-tabs>
    </el-card>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "social",
  },
  data() {
    return {
      activeName: "first",
    };
  },
  methods: {
    handleClick() {
      console.log(this.activeName);
    },
  },
};
</script>
<style lang="scss" scoped>
.user_body {
  .user_item {
    // color: #1e6bb8;
    margin-bottom: 10px;
    .card {
      color: #1e6bb8;
      font-size: 13px;
      line-height: 20px;
    }
  }
}
</style>
