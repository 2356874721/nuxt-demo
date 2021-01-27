<!--
 * @Author: sheriff
 * @Description: 文章列表
 * @Date: 2021-01-26 18:45:23
 * @LastEditors: sheriff
 * @LastEditTime: 2021-01-27 10:01:58
 * @LastEditDetails: 
-->
<template>
  <div class="article-list-page">article-list-page 文章类别：{{ type }}</div>
</template>

<script>
export default {
  props: {},
  data() {
    return {
      type: ""
    };
  },
  components: {},
  computed: {},
  watch: {},
  created() {},
  mounted() {
    // 文章的种类
    this.type = this.$route.params.type;
  },
  methods: {}
};
</script>

<style scoped lang="scss"></style>
