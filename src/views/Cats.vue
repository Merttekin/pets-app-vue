<template>
  <div>
    <h1>Cats</h1>
    <b-table striped hover :items="cats">
      <template slot="name" slot-scope="data">
        <router-link :to="`/pets/cats/${data.index}`">{{ data.value }}</router-link>
      </template>
    </b-table>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  computed: {
    ...mapState([
      'cats'
    ])
  }
};
</script>

<style>
</style>
