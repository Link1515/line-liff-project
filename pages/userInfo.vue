<template>
  <div class="userInfo">
    <h1>用戶資訊</h1>
    <h2>姓名: {{ userInfo.name }}</h2>
    <img class="avatar" :src="userInfo.picture" />
    <nuxt-link class="home__buttons__button button--secondary" to="/">
      返回首頁
    </nuxt-link>
  </div>
</template>

<script>
export default {
  computed: {
    userInfo() {
      return this.$liff.getDecodedIDToken();
    }
  }
};
</script>

<style scoped>
.userInfo {
  text-align: center;
}

.avatar {
  margin: auto;
  margin-bottom: 4rem;
  display: block;
  width: 200px;
  height: 200px;
  border-radius: 50%;
}
</style>
