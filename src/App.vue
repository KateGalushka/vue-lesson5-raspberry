<template>
	<product-panel :productCardList="raspberryList"/>
 </template>

<script>
import { raspberryList } from './constants/2_data_raspberry.js'
import ProductPanel from './components/ProductPanel.vue'

export default {
  name: 'App',

  components: {
	ProductPanel
  },

  data() {
	return {
		raspberryList
	}
  }
}
</script>

<style>

</style>
