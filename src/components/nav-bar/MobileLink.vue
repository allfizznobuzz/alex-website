<script>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

export default {
  props: {
    to: { type: String, required: true },
  },
  setup(props) {
    const route = useRoute()
    const isActive = computed(() => route.path === props.to)
    return { isActive }
  },
}
</script>

<template>
  <div bg-slate-800 class="container hover:text-gray-400 hover:bg-slate-700 transition duration-300 absolute">
    <router-link :to="to" pl-10 text-white pr-auto :class="{ active: isActive }" class="button">
      <slot />
    </router-link>
  </div>
</template>

<style>
.container {
    float:right;
    width:100%;
}

.button {
    display: block;
    padding: 10px;
    width: 100%;
}
</style>
