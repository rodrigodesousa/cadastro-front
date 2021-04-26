<template>
  <v-container>
    <v-row>
      <v-col>
        <v-data-table
          dense
          :headers="headers"
          :items="pessoas"
          item-key="name"
          class="elevation-1"
        ></v-data-table>
      </v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  data: () => ({
    headers: [
      { text: "Id", value: "id" },
      { text: "Nome", value: "nome" },
      { text: "Data de Nascimento", value: "nascimento" },
      { text: "CPF", value: "cpf" },
    ],
    pessoas: [],
  }),
  async mounted() {
    const response = await this.$http.get("pessoas");
    this.pessoas = response.body.content;
  },
};
</script>
