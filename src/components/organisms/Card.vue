<template>
  <div class="card">
    <div class="card-avatar">
    </div>
    <div class="card-name">
      {{ state.name }}
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue'

interface State {
  name: string;
}

export default defineComponent({
  props: {
    name: {
      type: String
    }
  },
  setup () {
    const state = reactive<State>({
      name: 'snowsphere'
    })

    return {
      state
    }
  }
})
</script>

<style lang="scss">
  .card {
    border: solid 1px #eee;

    .card-name {
      font-size: 1.5rem;
    }
  }
</style>
