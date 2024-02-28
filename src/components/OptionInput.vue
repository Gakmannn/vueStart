<template>
  <input type="text" :value="modelValue" @input="emitChange">
</template>

<script lang="ts">
export default {
  props: {
    modelValue: String
  },
  emits: ['update:modelValue'],
  methods: {
    emitChange(e:Event) {
      const target = e.target as HTMLInputElement
      this.$emit('update:modelValue', target.value)
    }
  }
}
</script>