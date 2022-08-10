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
  <div id="rightbox" bg-slate-800 class="py-2 hover:text-gray-400 hover:bg-slate-700 transition duration-300">
    <router-link :to="to" class="py-2 pl-2 text-white" :class="{ active: isActive }">
      <slot />
    </router-link>
  </div>
</template>

<style>
#rightbox{
  float:right;
  width:25%;}
</style>
