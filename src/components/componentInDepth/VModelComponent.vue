<template>
  <div>
    <input type="text" v-model="model" />
    <!--    <div>Parent bound v-model is: {{ model }}</div>-->
    <!--    <button @click="update">Increment</button>-->
  </div>
</template>

<script setup>
const [model, modifiers] = defineModel({
  set(value) {
    if (modifiers.capitalize) {
      return value.charAt(0).toUpperCase() + value.slice(1);
    }
    return value;
  },
});

function update() {
  model.value++;
}
</script>
