
<template>
  <div>
    <p>Counter is: {{ doubbleCounter }}</p>
    <p>Number of Clicks: {{ stringCounter }}</p>
  </div>
</template>

<script>
// more convinient way is mapping gatters to properties
import { mapGetters } from "vuex";
export default {
  // props: ['counter']
  computed: {
    // 3 dots allows to add own computed props (npm install --save-dev babel-preset-stage-2), and update babelrc with ["stage-2"]
    ...mapGetters(["doubbleCounter", "stringCounter"])
  }
};
</script>