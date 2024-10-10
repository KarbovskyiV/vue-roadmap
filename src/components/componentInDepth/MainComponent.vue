<template>
  <div>
    <span>{{ count }}</span>
    <BlogPost @increase-by="increaseCount" />
  </div>
</template>

<script setup>
import BlogPost from '@/components/componentInDepth/BlogPost.vue';
import { ref } from 'vue';

let count = ref(1);
function increaseCount(n) {
  count.value += n;
}
</script>
