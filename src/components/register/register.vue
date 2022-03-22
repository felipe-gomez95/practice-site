<template>
  <form action="" @submit="handleRegister($event)">
    <div>
      <input v-model="model.name" type="text" placeholder="nombre" />
    </div>
    <div>
      <select v-model="model.typeId" id="">
        <option value="opcion1">opcion 1</option>
        <option value="opcion2">opcion 2</option>
      </select>
      <input
        v-model="model.numberId"
        type="text"
        placeholder="numero de documento"
      />
    </div>
    <div>
      <button type="submit">enviar</button>
    </div>
  </form>
</template>

<script>
export default {
  data() {
    return {
      model: {
        name: "",
        typeId: "",
        numberId: "",
      },
    };
  },
  methods: {
    handleRegister(event) {
      event.preventDefault();
      console.log(this.model.name);
      console.log(this.model.typeId);
      console.log(this.model.numberId);
    },
  },
};
</script>
