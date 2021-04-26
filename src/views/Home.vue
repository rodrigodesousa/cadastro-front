<template>
  <div class="home">
    <ListaPessoas />
  </div>
</template>

<script>
// @ is an alias to /src
import ListaPessoas from "@/components/ListaPessoas.vue";

export default {
  name: "Home",
  components: {
    ListaPessoas,
  },
};
</script>
