<template>
  <div>
    <div class="loading" v-if="loading">
      <img src="../assets/loading.gif" alt />
    </div>
    <div>
      <ul>
        <li>
          <div class="toobar">
            <span>全部</span>
            <span>精华</span>
            <span>分享</span>
            <span>问答</span>
            <span>招聘</span>
          </div>
        </li>
        <li v-for="post in posts"></li>
      </ul>
    </div>
    <li></li>
  </div>
</template>

<script>
export default {
  name: "Postlist",
  data() {
    return {
      loadign: false,
      posts: []
    };
  },
  methods: {
    getData() {
      this.$http
        .get("https://cnodejs.org/api/v1/topics", {
          page: 1,
          limit: 20
        })
        .then(res => {
          this.isLoading = false; //加载成功，去除动画
          this.posts = res.data.data;
        })
        .catch(function(err) {
          //处理返回失败后的问题
          console.log(err);
        });
    }
  }
};
</script>

<style scoped>
</style>
