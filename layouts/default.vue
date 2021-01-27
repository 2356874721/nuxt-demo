<template>
  <div>
    <Layout>
      <Header>
        <Menu mode="horizontal" :theme="theme1">
          <MenuItem name="1">
            <Icon type="ios-paper" />
            <nuxt-link to="/">首页</nuxt-link>
          </MenuItem>
          <Submenu name="2">
            <template slot="title">
              <Icon type="ios-stats" />
              文章
            </template>
            <MenuGroup title="类别一">
              <MenuItem name="3-1">
                <nuxt-link to="/article/technology/list">技术</nuxt-link>
              </MenuItem>
            </MenuGroup>
            <MenuGroup title="类别二">
              <MenuItem name="3-2">
                <nuxt-link to="/article/reading/list">读书</nuxt-link>
              </MenuItem>
            </MenuGroup>
          </Submenu>
          <MenuItem name="3">
            <Icon type="ios-construct" />
            关于我们
          </MenuItem>
        </Menu>
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
      theme1: "dark"
    };
  }
};
</script>

<style lang="scss" scoped></style>
