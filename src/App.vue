<template>
  <PageHeader v-bind:avatar="avatar" />
</template>

<script>
import PageHeader from '@/modules/PageHeader.vue'
import { reactive, toRefs } from 'vue'

export default {
  components: { PageHeader },
  setup () {
    const avatar = reactive({ avatar: 'https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png' })
    return {
      ...toRefs(avatar)
    }
  }
}
console.log('LS')
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.title {
  font-size: 23px;
}

.flex-grow,
.grow {
  flex-grow: 1;
}
</style>
