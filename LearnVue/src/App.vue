<template>
  <h1>Dynamic Components</h1>
  <p>App.vue switches between which component to show.</p>
  <button @click="toggleValue = !toggleValue">Switch component</button>
  <component :is="activeComp"></component>
</template>

<script>
export default {
  data() {
    return {
      toggleValue: true,
    };
  },
  computed: {
    activeComp() {
      if (this.toggleValue) {
        return "comp-one";
      } else {

        //console.log(this.toggleValue)
        return "comp-two";
      }
    },
  },
};
</script>

<style>
#wrapper {
  display: flex;
  flex-wrap: wrap;
}

#wrapper>div {
  border: dashed black 1px;
  margin: 10px;
  padding: 10px;
  background-color: lightgreen;
}
</style>
