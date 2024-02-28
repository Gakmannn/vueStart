<template>
  <input type="text" :value="title" @input="emitChange">
</template>

<script setup lang="ts">
const props = defineProps(['title', 'checkFunc'])
const emit = defineEmits(['update:title', 'update:check'])
const emitChange = (e:Event)=>{
  const target = e.target as HTMLInputElement
  emit('update:title', target.value)
  if (props.checkFunc) {
    emit('update:check', props.checkFunc(target.value))
  }
} 
</script>