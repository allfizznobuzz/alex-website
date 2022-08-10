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
  <router-link :to="to" class="py-2 px-2 text-white hover:text-gray-400 hover:bg-slate-700 rounded transition duration-300" :class="{ active: isActive }">
    <slot />
  </router-link>
</template>
