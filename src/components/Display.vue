<template>
  <input type="text" name="display" :value="value">
</template>

<script>
export default {
  name: 'Display',
  props: {
    value: String
  }
}
</script>
