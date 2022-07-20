<template>
	<div class="nav-bar__item">
		<img :src="navBarItem.iconPath">
		<p>{{navBarItem.title}}</p>
	</div>
</template>

<script>
export default {
	name: "nav-bar-item",
	props: {
		navBarItem: {
			type: Object,
			required: true,
		},
	},
}
</script>

<style lang="scss" scoped>
	.nav-bar__item {
		min-width: 75px;
		min-height: 49px;
		font-size: 10px;
		line-height: 100%;
		img{

		}
		p{

		}
	}
</style>