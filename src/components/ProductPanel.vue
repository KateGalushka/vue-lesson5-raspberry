<template>
	<div class="container">
		<product-card
		 v-for="card in productCardList" :key="card.id" 
		 :card-data="card"
		 />
	</div>
</template>

<script>
import ProductCard from './ProductCard.vue'

export default {
	name: "ProductPanel",

	components: { ProductCard },

	props: {
		productCardList: {
			type: Array,
			default: () => []
		},
	}
}
</script>

<style lang="css" scoped>
.container {
	display: flex;
	background-color: #000;
	padding: 10px;
	flex-wrap: wrap;
	max-width: 50vw;
	margin: 50px auto;
	gap: 20px;
}
</style>