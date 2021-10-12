<template>
  <v-app>
    <div class="table">
      <t-document></t-document>
    </div>
  </v-app>
</template>

<script>
import TDocument from './components/TDocument/TDocument.vue';

export default {
  components: { TDocument },
  name: 'App',
  data() {
    return {
      testV: 'Hello',
    };
  },
};
</script>

<style lang="scss">
html {
  margin: 0;
  padding: 0;
}
body {
  margin: 0;
  padding: 10px;
}
.table {
  width: 100%;
  height: calc(100vh - 20px);
}
</style>
