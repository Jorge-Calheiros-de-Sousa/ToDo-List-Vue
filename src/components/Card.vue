<template>
  <div>
    <b-card v-for="item in items" :key="item.id" class="my-2">
      <b-card-title>
        <b-form-input
          v-model="item.title"
          type="text"
          required
          size="lg"
          class="border-0"
        ></b-form-input>
      </b-card-title>
      <b-card-text>
        <b-form-textarea
          v-model="item.description"
          type="text"
          required
          class="border-0"
        ></b-form-textarea>
      </b-card-text>

      <b-button variant="danger" class="mx-2" @click="$emit('delete', item.id)"
        >Excluir</b-button
      >
    </b-card>
  </div>
</template>

<script>
export default {
  props: {
    items: [],
  },
};
</script>

<style>
</style>