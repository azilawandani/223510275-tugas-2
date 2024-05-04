<template>
  <div id="app">
    <input type="text" v-model="inputText" @input="onInput">
    <p :class="{ 'active': isActive, 'highlight': isHighlight }" :style="{ 'font-size': fontSize + 'px' }">Text: {{ inputText }}</p>
    <button @click="toggleHighlight">Toggle Highlight</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isActive: false,
      isHighlight: false,
      fontSize: 16
    };
  },
  methods: {
    onInput() {
      console.log('Input:', this.inputText);
    },
    toggleHighlight() {
      this.isHighlight = !this.isHighlight;
    }
  }
};
</script>

<style scoped>
.active {
  color: green;
}
.highlight {
  font-weight: bold;
}
.paragraf {
  font-size: 25px;
  color: red;
}
</style>
