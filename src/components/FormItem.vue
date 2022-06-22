<template>
  <div>
    <b-form class="my-3">
      <b-form-group label="Titulo da tarefa" id="title">
        <b-form-input
          id="title"
          placeholder="Digite o titulo da tarefa"
          v-model="title"
        >
        </b-form-input>
      </b-form-group>
      <b-form-group label="Descrição da tarefa" id="description">
        <b-form-textarea
          id="description"
          placeholder="Digite a descrição da tarefa"
          v-model="description"
        >
        </b-form-textarea>
      </b-form-group>
      <b-button
        type="button"
        variant="primary"
        class="my-2"
        @click="
          $emit('submit', {
            id: length + 1,
            title: title,
            description: description,
          })
        "
        >Adicionar</b-button
      >
    </b-form>
  </div>
</template>

<script>
export default {
  props: ["length"],
  data: function () {
    return {
      id: "",
      title: "",
      description: "",
    };
  },
};
</script>

<style>
</style>