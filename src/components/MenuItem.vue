<template>
	<div class="menu__item">
		<div class="menu__item_icon">
			<img :src="menuItem.iconPath">
		</div>
		<div class="menu__item_title">{{menuItem.title}}</div>
		<img class="menu__item_arrow" :src="require('../assets/Arrow.png')">
	</div>
</template>

<script>
export default {
	name: "menu-item",
	props: {
		menuItem: {
			type: Object,
			required: true,
		}
	}
}
</script>

<style lang="scss" scoped>
	.menu__item {
		position: relative;
		min-height: 64px;
		width: 100%;
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		align-items: center;
		gap: 12px;
		border-bottom: 1px solid #0909094D;
		margin-top: -1px;
		font-size: 16px;
		line-height: 120%;
		&_icon {
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
		}
		&_title {

		}
		&_arrow {
			position: absolute;
			right: 0;
		}
	}
</style>