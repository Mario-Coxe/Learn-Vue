<template>
  <h3>Local Component</h3>
  <p>The CompOne.vue component is a local component and can only be used inside App.vue.</p>
  <comp-one />
  <comp-two />
</template>

<script>

import CompOne from './components/CompOne.vue';

export default {
  components: {
    'comp-one': CompOne
  }

}
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
