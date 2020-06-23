<template>
  <div>
    <div>
      <Display :value="input"/>
    </div>
    <div>
      <Button label="7" @newInput="addInput"/>
      <Button label="8" @newInput="addInput"/>
      <Button label="9" @newInput="addInput"/>
      <Button label="/" @newInput="addInput"/>
    </div>
    <div>
      <Button label="4" @newInput="addInput"/>
      <Button label="5" @newInput="addInput"/>
      <Button label="6" @newInput="addInput"/>
      <Button label="*" @newInput="addInput"/>
    </div>
    <div>
      <Button label="1" @newInput="addInput"/>
      <Button label="2" @newInput="addInput"/>
      <Button label="3" @newInput="addInput"/>
      <Button label="-" @newInput="addInput"/>
    </div>
    <div>
      <Button label="0" @newInput="addInput"/>
      <Button label="." @newInput="addInput"/>
      <Button label="=" @newInput="calculateInput"/>
      <Button label="+" @newInput="addInput"/>
    </div>
    <div>
      <Button label="Clear" @newInput="clearInput"/>
    </div>
  </div>
</template>

<script>

import Button from "./Button"
import Display from "./Display"

export default {
  name: 'Calculator',
  components: { Button, Display },
  data () {
    return {
      input: ''
    }
  },
  methods: {
    addInput (newInput) {
      if (this.input == '0')
        this.input = ''

      this.input = `${this.input}${newInput}`
    },
    calculateInput () {
      this.input = `${eval(this.input)}`
    },
    clearInput () {
      this.input = '0'
    }
  }
}
</script>
