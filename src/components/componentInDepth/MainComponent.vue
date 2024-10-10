<template>
  <div>
    <!--    <span>{{ count }}</span>-->
    <!--    <BlogPost @increase-by="increaseCount" />-->
    <!--  <VModelComponent v-model="countModel"/>-->
    <VModelComponent v-model.capitalize="myText" />
  </div>
</template>

<script setup>
import BlogPost from '@/components/componentInDepth/EmitComponent.vue';
import { ref } from 'vue';
import VModelComponent from '@/components/componentInDepth/VModelComponent.vue';

const countModel = ref(1);
const myText = ref('MyText');
/*
let count = ref(1);
function increaseCount(n) {
  count.value += n;
}
*/
</script>
