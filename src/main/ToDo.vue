<template>
  <div>
    <nav-bar />
    <b-container>
      <form-item @submit="createItem" :length="items.length" />
      <card :items="items" @delete="deleteItem" />
    </b-container>
  </div>
</template>

<script>
import NavBar from "../components/NavBar.vue";
import FormItem from "../components/FormItem.vue";
import Card from "../components/Card.vue";
export default {
  components: { NavBar, Card, FormItem },
  data: function () {
    return {
      items: [
        {
          id: 1,
          title: "Fazer bolo",
          description: "Comprar uma farinha para fazer bolo",
        },
        {
          id: 2,
          title: "Tarefa",
          description: "Tarefa exemplo",
        },
      ],
    };
  },
  methods: {
    deleteItem(id) {
      const newItems = this.items;
      const index = newItems.findIndex((item) => item.id === id);
      newItems.splice(index, 1);
      this.items = newItems;
    },
    createItem(item) {
      this.items.push(item);
    },
  },
};
</script>

<style>
</style>