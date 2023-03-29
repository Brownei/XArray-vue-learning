<template>
  <div>
    <XArray v-model="myArray" />
    <div v-for="array in myArray">
      <input type="text" :value="array">
    </div>
    <input type="text" v-model="emptyInput">
    {{emptyInput}}
  </div>
</template>

<script>
import XArray from './components/XArray.vue';

export default {
  components: {
    XArray,
  },
  data: () => {
    return {
      myArray: ['one', 'two'],
      myResult1: `<div>
        <input value="one">
        <input value="two">
        <input value="">
      </div>`,
      emptyInput: ''
    };
  },
};
</script>
