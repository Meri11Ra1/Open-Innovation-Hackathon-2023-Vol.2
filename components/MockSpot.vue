<template>
  <div>
    <v-row>
      <v-col>{{ spotData.congestion }}</v-col>
      <v-col>{{ spotData.name }}</v-col>
      <v-col>{{ spotData.address }}</v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  props: {
    spotData: Object
  }
}
</script>

<style>

</style>
