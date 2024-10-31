<template>
  <a-table :data="tableData" :columns="columns" />
</template>

<script>
import { ref, defineComponent } from "vue";

export default defineComponent({
  name: "VersionList",
  setup() {
    const tableData = ref([]);
    const columns = [
      {
        title: "Node Version",
        dataIndex: "version",
      },
      {
        title: "NPM Version",
        dataIndex: "npm",
      },
      {
        title: "Date",
        dataIndex: "date",
      },
    ];

    const getData = async () => {
      fetch("https://nodejs.org/download/release/index.json")
        .then((res) => res.json())
        .then((res) => (tableData.value = res));
    };

    getData();

    return {
      tableData,
      columns,
    };
  },
});
</script>
