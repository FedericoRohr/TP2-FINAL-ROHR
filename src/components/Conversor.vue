<template >

  <section class="src-components-conversor">
    <h1>Conversor de Temperatura</h1>

    <label for="celcius">Ingrese Temperatura °C </label>
    <input id="celcius" class="form-control" v-model="celcius" type="number" />

    <br> <br>
    <label>Conversion de temperatura °F :</label> <label :style="{color: getColor}">{{ getFarnheit }}</label>
    <br> <br>
    <label>Conversion de temperatura °K :</label> <label :style="{color: getColor}">{{ getKelvin }}</label>
    <br />
    <br />

  </section>

</template>

<script>

export default {
  name: 'src-components-conversor',
  props: [],
  mounted() {

  },
  data() {
    return {
      celcius: null,
    }
  },
  methods: {

  },
  computed: {
    getFarnheit() {
      if (this.celcius == null) {
        return
      }
      return (this.celcius * 1.8) + 32
    },
    getKelvin() {
      if (this.celcius == null) {
        return
      }
      return Number(this.celcius) + 273.15
    },
    getColor(){
      if(this.celcius<=0){
        return 'blue'
      }else if(this.celcius>=0 && this.celcius<15){
        return 'magenta'
      }else{
        return 'red'
      }
    }
  }
}


</script>

<style scoped lang="css">

</style>
