<!--
    页头组件
    Author: Laosun
    Create Date: 2023-02-25 10:22
-->
<template>
    <el-menu :default-active="activeIndex" class="el-menu-demo" mode="horizontal" :ellipsis="false" @select="handleSelect">
        <el-menu-item index="0" class="title">TEST</el-menu-item>
        <el-menu-item index="1">Processing Center</el-menu-item>
        <div class="flex-grow" />
        <el-sub-menu index="2">
            <template #title><el-avatar v-bind:src="avatar" title="头像"/></template>
            <el-menu-item index="2-1">item one</el-menu-item>
            <el-menu-item index="2-2">item two</el-menu-item>
            <el-menu-item index="2-3">item three</el-menu-item>
            <el-sub-menu index="2-4">
                <template #title>item four</template>
                <el-menu-item index="2-4-1">item one</el-menu-item>
                <el-menu-item index="2-4-2">item two</el-menu-item>
                <el-menu-item index="2-4-3">item three</el-menu-item>
            </el-sub-menu>
        </el-sub-menu>
    </el-menu>
</template>
<script>
import { ElMenu, ElMenuItem, ElSubMenu, ElAvatar } from 'element-plus'
import 'element-plus/dist/index.css'

export default {
  name: 'PageHeader',
  props: {
    avatar: String
  },
  components: { ElMenu, ElMenuItem, ElSubMenu, ElAvatar }
}
console.log('LS')
</script>
