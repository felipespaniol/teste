<template>
  <div>
    <h1>{{ message }}</h1>
    <button @click="editMessage">Edit Text</button>
    <button v-if="message === 'Text has been updated!'" @click="resetMessage">Reset Text</button>
  </div>
</template>

<script>
export default {
  name: 'EditMessage',
  data() {
    return {
      message: 'Original text2'
    };
  },
  methods: {
    editMessage() {
      this.message = 'Text has been updated!';
    },
    resetMessage() {
      this.message = '';
    }
  }
};
</script>

<style scoped>
button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
}

h1 {
  color: #000;
}
</style>