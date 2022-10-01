<template>
  <div>
    Item
    <router-link to="1">Item1</router-link>
    <router-link to="2">Item2</router-link>
    {{ $route.params.id }}
  </div>
</template>

<script>
export default {
  created() {
    //同じコンポーネント内で表示切り替えしているだけなので一度しか呼ばれない
    //同じコンポーネント内の表示切り替え時に何か発火させたい場合は、watchやナビゲーションガードを使う
    console.log("created");
  },
  watch: {
    $route(to, from) {
      //routeオブジェクトが切り替わったら、この関数が実行される
      console.log(to, from);
    },
  },
};
</script>

<style></style>
