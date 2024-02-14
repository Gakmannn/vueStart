<script setup lang="ts">
import TemplateButton from './components/TemplateButton.vue'
import CounterButton from './components/CounterButton.vue'
import OptionsApi from './components/OptionsApi.vue'
</script>

<template>
  <header>
    header
  </header>  
  <CounterButton v-bind:start="10"/>
  <CounterButton :start="15"/>
  <CounterButton/>
  <CounterButton/>
  <CounterButton/>
  <CounterButton/>
  <CounterButton/>
  <TemplateButton>Content from parent</TemplateButton>
  <TemplateButton></TemplateButton>
  <br>
  <OptionsApi/>
</template>

<style scoped>

</style>
