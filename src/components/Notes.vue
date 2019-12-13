<template lang="html">
  <div class="ui container notes">
    <h4 class="ui horizontal divider header">
      <i class="paw icon"></i>
      Notes App _ Vue.js + Vuex Example
    </h4>
    <a class="ui right floated basic violet button">添加笔记</a>
    <div class="ui divided items">
      <note v-for="entity in entities" :key="entity.id" v-bind:entity="entity"></note>
      <span class="ui small disabled header">
        还没有笔记，请按下“添加笔记”按钮。
      </span>
    </div>
  </div>
</template>

<script>
import Note from './Note'
import { mapGetters } from 'vuex'
export default {
  computed: {
    ...mapGetters([
      'entities'
    ])
  },
  components: {
    Note
  }
}
</script>

<style lang="css" scoped>
</style>
