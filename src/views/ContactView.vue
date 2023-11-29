<script>
export default {
  data() {
    return {
      show: false
    };
  },
  methods: {
    changeColor() {
      this.show = !this.show;
    }
  }
};
</script>

<template>
  <div class="container">
    <h1 :class="{ 'text-red-500 text-4xl': show }">hello contact page</h1>
    <button @click="changeColor">change color</button>
  </div>
</template>
