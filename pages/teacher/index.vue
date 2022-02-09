<template>
  <div>
    <div>
      Öğretmenleri Görüntüleme Sayfası
    </div>
    <br />
    <v-text-field
      v-model="labelValue"
      solo
      label="Alınacak Değer"
      clearable
    />
    <v-btn
      outlined
      color="primary"
      @click="updateLabel"
    >
      Alınacak Değeri Güncelle
    </v-btn>
    <v-text-field
      v-model="value"
      solo
      :label="inputLabel"
      clearable
    />
    <v-btn
      outlined
      color="normal"
      @click="routeToHome"
    >
      Geri
    </v-btn>
    <v-btn
      outlined
      color="primary"
      @click="showValue"
    >
      Değeri Görüntüle
    </v-btn>
  </div>
</template>

<script>
export default {
  data () {
    return {
      labelValue: '',
      inputLabel: '',
      value: ''
    }
  },
  methods: {
    routeToHome () {
      this.$router.push('/')
    },
    showValue () {
      console.log(this.value)
    },
    updateLabel () {
      this.inputLabel = this.labelValue
    }
  }
}
</script>
