<template>
  <div>
    <md-table v-model="users" :table-header-color="tableHeaderColor">
      <md-table-row slot="md-table-row" slot-scope="{ item }">
        <md-table-cell md-label="ID">{{ item.id }}</md-table-cell>
        <md-table-cell md-label="Name">{{ item.name }}</md-table-cell>
        <md-table-cell md-label="Clients">{{ item.clients }}</md-table-cell>
        <md-table-cell md-label="Contact">{{ item.contact }}</md-table-cell>
      </md-table-row>
    </md-table>
  </div>
</template>

<script>
export default {
  name: "ordered-table",
  props: {
    tableHeaderColor: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      selected: [],
      users: [
        {
          id: 1,
          name: "Dakota Rice",
          clients: "100",
          contact: "+91 123 456 7890"
        },
        {
          id: 2,
          name: "Minerva Hooper",
          clients: "20",
          contact: "+91 123 456 7890"
        },
        {
          id: 3,
          name: "Sage Rodriguez",
          clients: "42",
          contact: "+91 123 456 7890"
        },
        {
          id: 4,
          name: "Philip Chaney",
          clients: "25",
          contact: "+91 123 456 7890"
        },
      ],
    };
  },
};
</script>
