<template>
  <div class="blog-post">
    <button @click="$emit('increaseBy', 1)">Increase by 1</button>
  </div>
</template>

<script setup>
const emit = defineEmits({
  // No validation
  click: null,
  increaseBy: Number,

  // Validate submit event
  submit: ({ email, password }) => {
    if (email && password) {
      return true;
    } else {
      console.warn('Invalid submit event payload!');
      return false;
    }
  },
});

function submitForm(email, password) {
  emit('submit', { email, password });
}
</script>
