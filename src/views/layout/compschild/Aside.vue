<template>
  <div :class="istubiao ? 'baifenbai' : 'content'">
    <el-menu
      :default-active="$route.path"
      background-color="#002033"
      text-color="#fff"
      active-text-color="#ffd04b"
      router
      :collapse="istubiao"
    >
      <slot></slot>
      <el-menu-item index="/">
        <i class="el-icon-s-home"></i>
        <span slot="title">首页</span>
      </el-menu-item>
      <el-menu-item index="/detect">
        <i class="el-icon-menu"></i>
        <span slot="title">健康分析</span>
      </el-menu-item>
      <el-menu-item index="/admin">
        <i class="el-icon-s-custom"></i>
        <span slot="title">管理员</span>
      </el-menu-item>
      <el-menu-item index="/my">
        <i class="el-icon-setting"></i>
        <span slot="title">个人设置</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: '',
  components: {},
  props: {
    istubiao: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {}
  },
  computed: {},
  watch: {},
  created() {},
  mounted() {},
  methods: {},
}
</script>

<style scoped lang="less">
.baifenbai {
  width: 100%;
}
.content {
  width: 200px;
  .tac {
    width: 100% !important;
  }
}
.el-menu {
  height: 100%;
}
</style>
