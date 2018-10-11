<template>
  <div>
    <h1>Kaalu teisendamine</h1>
    <h4>Sisesta kaal kilogrammides:</h4>
    <input type="number" v-model="kg">
    <table v-if="kg !==0">
      <tr>
        <td>Grammid</td>
        <td>{{ convertKg(1000) + ' g' }}</td>
      </tr>
      <tr>
        <td>Naelad</td>
        <td>{{ convertKg(2.2046) + ' lb' }}</td>
      </tr>
      <tr>
        <td>Untsid</td>
        <td>{{ convertKg(35.2739) + ' oz' }}</td>
      </tr>
    </table>
    
  </div>
</template>

<script>
export default {
  name: 'Konverter',
  data () {
    return { 
      kg: 0
    }
  },
  methods: {
    convertKg(multiplier) {
      
      return (this.kg !== 0) ? (this.kg * multiplier).toFixed(2) : 0

    }
    
  }
  
}
</script>
<!--this.users... kasutab siis seda kasutajat, defineerib-->
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>


</style>
