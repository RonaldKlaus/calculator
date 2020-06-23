<template>
  <button :value="label" @click="onClick(label)">
    {{ label }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    label: String
  },
  methods: {
    onClick (value) {
      this.$emit('newInput', value)
    }
  }
}
</script>
