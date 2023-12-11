<template>
  <div class="logo">
    <!--    <img :src="websiteConfig.logo" alt="" :class="{ 'mr-2': !collapsed }" />-->
    <n-icon color="#69AA46" size="25">
      <leaf />
    </n-icon>
    <h2 v-show="!collapsed" class="title">&nbsp;&nbsp;{{ websiteConfig.title }}</h2>
  </div>
</template>

<script lang="ts">
  import { websiteConfig } from '@/config/website.config';
  import { Leaf } from '@vicons/ionicons5';
  export default {
    name: 'Index',
    components: { Leaf },
    props: {
      collapsed: {
        type: Boolean,
      },
    },
    data() {
      return {
        websiteConfig,
      };
    },
  };
</script>

<style lang="less" scoped>
  .logo {
    display: flex;
    align-items: center;
    justify-content: center;
    height: 64px;
    line-height: 64px;
    overflow: hidden;
    white-space: nowrap;

    img {
      width: auto;
      height: 32px;
    }

    .title {
      margin: 0;
    }
  }
</style>
