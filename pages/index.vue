<template>
  <div>
    <v-btn
      outlined
      color="indigo"
      @click="routeToTeacher"
    >
      Öğretmen İşlemleri
    </v-btn>
  </div>
</template>

<script>
export default {
  methods: {
    routeToTeacher () {
      this.$router.push('teacher')
    }
  }
}
</script>
