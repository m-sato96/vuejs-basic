<template>
  <div>
    404 ページが存在しません
    <button @click="goToHome">トップへ戻る</button>
  </div>
</template>

<script>
export default {
  methods: {
    goToHome() {
      this.$router.push("/");
    },
  },
};
</script>

<style></style>
