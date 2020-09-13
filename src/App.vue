<template>
  <div>
    <div
      v-for="(item,index) in message"
      :key="index"
      :class="{active:currentIndex===index}"
      @click="itemClick(index)"
    >{{item}}</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      message: ["哈哈哈", "啦啦啦", "呵呵呵"],
    };
  },
  methods: {
    itemClick(index) {
      this.currentIndex = index;
    },
  },
};
</script>

<style>
.active {
  color: red;
}
</style>
