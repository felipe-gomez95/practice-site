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
      <select v-model="model.country">
        <option
          v-for="country in countries"
          :key="country.value"
          :value="country.value"
        >
          {{ country.name }}
        </option>
      </select>
      <select v-model="model.state">
        <option value="1"></option>
        <option value="2"></option>
        <option value="3"></option>
      </select>
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
        country: "",
        state: "",
      },
      countries: [
        {
          name: "Colombia",
          value: 57,
        },
        {
          name: "Bolivia",
          value: 24,
        },
        {
          name: "Peru",
          value: 48,
        },
      ],
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
