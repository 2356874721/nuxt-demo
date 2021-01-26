<!--
 * @Author: sheriff
 * @Description: 导航栏
 * @Date: 2021-01-26 17:58:28
 * @LastEditors: sheriff
 * @LastEditTime: 2021-01-26 19:22:06
 * @LastEditDetails: 
-->
<template>
  <div class="titlebar-page" wrap="mr-30">
    <div class="show-title" wrap="c-fff" @click="toPath">{{ title }}</div>
    <div class="hide-title">
      <nuxt-link v-for="item in list" :key="item" :to="item.path">{{
        item.title
      }}</nuxt-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "TitleBar",
  props: {
    title: {
      type: String,
      default: ""
    },
    link: {
      type: String,
      default: ""
    },
    list: {
      type: Array,
      default: []
    }
  },
  data() {
    return {};
  },
  components: {},
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  methods: {
    toPath() {
      if (!this.link) return;
      this.$router.push({ path: this.link });
    }
  }
};
</script>

<style scoped lang="scss">
.titlebar-page {
  display: inline-block;
  position: relative;
  .show-title {
    cursor: pointer;
    font-weight: bold;
  }
  .hide-title {
    display: none;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    top: bottom;
  }
  &:hover {
    & > .hide-title {
      display: block;
    }
  }
}
</style>
