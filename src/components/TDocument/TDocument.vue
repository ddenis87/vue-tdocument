<template>
  <div class="tdocument">
    <div class="toolbar">
      <t-document-toolbar></t-document-toolbar>
    </div>
    <div class="sheet"></div>
  </div>
</template>

<script>
import TDocumentToolbar from './TDocumentToolbar.vue';

export default {
  name: 'TDocument',
  components: {
    TDocumentToolbar,
  },
};
</script>

<style lang="scss" scoped>
.tdocument {
  display: grid;
  grid-template-areas: "toolbar" "sheet";
  grid-template-rows: 44px 1fr;
  grid-template-columns: 1fr;
  width: 100%;
  height: 100%;

  .toolbar {
    grid-area: toolbar;
    overflow: hidden;
    // border: thin solid rgba(0, 0, 0, .2);
    border-bottom: 0;
  }

  .sheet {
    grid-area: sheet;
    border: thin solid black;
  }
}
</style>
