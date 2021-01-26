<template>
  <div>
    <Layout>
      <Header>
        <div wrap="flex jc-fs ai-c">
          <TitleBar title="分类1" :list="list1" />
          <TitleBar title="分类2" :list="list2" />
          <!-- <TitleBar title="分类1" link="/home" :list="list1" />
          <TitleBar title="分类1" link="/home" :list="list1" />
          <TitleBar />
          <TitleBar /> -->
        </div>
      </Header>
      <Content>
        <!-- 相当于 router-view -->
        <Nuxt />
      </Content>
      <Footer>Footer</Footer>
    </Layout>
  </div>
</template>

<script>
export default {
  data() {
    return {
      list1: [
        {
          title: "子分类1",
          path: "/article/list"
        }
      ],
      list2: [
        {
          title: "子分类1",
          path: "/article/list"
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped></style>
