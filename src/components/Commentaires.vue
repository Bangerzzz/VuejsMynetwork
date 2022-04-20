<template v-if="commentaires">
  <div class="row com" v-for="(c, i) in commentaires" :key="i">
    <hr />
    <div class="col-12 d-flex justify-content-between">
      <h4>{{ c.pseudo }}</h4>
      <p>
        Ajouté le :
        {{
          new Date(c.dt).getDate() +
          "/" +
          (new Date(c.dt).getMonth() + 1) +
          "/" +
          new Date(c.dt).getFullYear()
        }}
        à {{ new Date(c.dt).getHours() }}h{{ new Date(c.dt).getMinutes() }}
      </p>
    </div>
    <div class="col-12">
      <p>{{ c.contenu }}</p>
    </div>
  </div>
  <hr />
</template>

<script>
export default {
  props: ["commentaires"],
  setup() {}
};
</script>
