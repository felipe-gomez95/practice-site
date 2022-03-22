<template>
  <form @submit="handleRegister">
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
      // Acá va el codigo para enviar la data a strapi

      // Las datos ingresados por el usuario estan en el modelo, si
      // quiere acceder a la variable nombre por ejemplo se usa this.model.name
    },
  },
};
</script>
