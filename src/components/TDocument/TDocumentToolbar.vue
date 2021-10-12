<template>
  <div class="tdocument-toolbar">
    <v-tabs v-model="currentList"
              align-with-title>
      <v-tab v-for="list in lists"
             :key="list.name">{{ list.title }}</v-tab>
    </v-tabs>
  </div>
</template>

<script>
export default {
  name: 'TDocumentToolbar',
  props: {
    lists: {
      type: Array,
      default() {
        return [
          { name: 'sheet1', title: 'Лист 1' },
        ];
      },
    },
  },
};
</script>
