<template>
  <button @click="increment" @mouseover="sayHi">{{ countD }} {{text}} {{ superText }}</button>  
</template>

<script lang="ts">
export default {
  props: {
    count:{
      type:Number,
      default: 3
    }, 
    text: {
      type: String,
      required: true
    },
    superText: String
  },
  data() {
    return {
      countD: this.count ? this.count : 0
    }
  },
  methods: {
    increment(e:MouseEvent) {
      this.countD++
      if (this.countD == 5) {
        this.$emit('hide')
      }
    },
    sayHi() {
      console.log('Hi from button')
    }
  },
  computed: {
    color() {
      return this.countD % 2 ? 'blue' : 'orange'
    }
  },
  beforeCreate() {
    console.log('bC', Date.now())
  },
  created() {
    console.log('C', Date.now())
  },
  beforeMount() {
    console.log('bM', Date.now())
  },
  mounted() {
    console.log('M', Date.now())
  },
  beforeUpdate() {
    console.log('bUpd', Date.now())
  },
  updated() {
    console.log('Upd', Date.now())
  },
  beforeUnmount() {
    console.log('bUnm', Date.now())
  },
  unmounted() {
    console.log('Unm', Date.now())
  }
}
</script>