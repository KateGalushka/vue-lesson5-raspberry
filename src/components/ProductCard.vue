<template>
	<a href="#">
		<div class="container">
			<img class="product__img" :src="cardData.imgSrc">
			<div class="logo-container">
				<img class="logo" :src="cardData.logo">
				<h5> {{ cardData.companyTitle }}</h5>
			</div>
			<p class="descr">
				{{ cardData.description }}
			</p>
		</div>
	</a>
</template>

<script>
	export default {
		name:"ProductCard",

		props:{
			cardData: {
				type: Object,
				default: ()=>({}),
			},
		},
	}
</script>

<style lang="css" scoped>
.container {
	display: flex;
	flex-direction: column;
	color: #fff;
	border-radius: 10px;
}
.logo-container {
	display: flex;
	justify-content: flex-start;
	align-items: center;
	margin: 0;
	padding: 0;
}
.logo-container img{
	width: 10px;
	height: 10px;
}
.product__img {
	border-radius: 12px;
	width: 150px;
	height: 130px;

}
a{
	text-decoration: none;
	margin: 0;
	padding: 0;
	color: inherit;
}
h5{
	margin: 0;
	padding: 5px;
}
p{
	margin: 10px 0 0;
}
</style>