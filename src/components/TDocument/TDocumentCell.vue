<template>
  <div class="tdocument-cell"
       :class="`tdocument-cell_${cellForm}`">
    <span v-html="value"></span>
  </div>
</template>

<script>
export default {
  model: {
    prop: 'cellValue',
  },
  name: 'TDocumentCell',
  props: {
    cellForm: { type: String, default: 'body' },
    cellType: { type: String, default: 'string' },
    cellValue: { type: [String, Number, Boolean, Date, Object], default: null },
  },
  data() {
    return {
      // value: '',
      // type: this.cellType,
    };
  },
  computed: {
    value() {
      return this.cellValue || '';
    },
  },
};
</script>

<style lang="scss" scoped>
@import './TDocumentCell.scss';

.tdocument-cell {
  border-right: $cell_border_grid;
  border-bottom: $cell_border_grid;

  &_body {
    width: $cell_body_width;
    height: $cell_body_height;
  }

  &_title {
    width: $cell_title_width;
    height: $cell_title_height;
    background-color: $cell_title_background_color;
    border-right: $cell_border_title;
    border-bottom: $cell_border_title;
    border-left: $cell_border_title;
  }
}
</style>
