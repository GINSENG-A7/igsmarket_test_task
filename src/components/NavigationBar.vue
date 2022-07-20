<template>
	<div class="background">
		<div class="icons__flex_container">
			<nav-bar-item v-for="navBarItem in navBarItems" :navBarItem="navBarItem" :key="navBarItem.id"></nav-bar-item>
		</div>
		<div class="virtual__stick"></div>
	</div>
</template>

<script>
export default {
	name: "nav-bar",
	props: {
		navBarItems: {
			type: Array,
			required: true,
		},
	},
}
</script>

<style lang="scss" scoped>
	.background {
		width: 100%;
		min-height: 90px;
		position: fixed;
		bottom: 0;
		background: rgba(154, 152, 154, 0.94);
		backdrop-filter: blur(20px);
		border-top-left-radius: 16px;
		border-top-right-radius: 16px;
		border-bottom-left-radius: 20px;
		border-bottom-right-radius: 20px;
		.icons__flex_container {
			margin-top: 6px;
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
		}
		.virtual__stick {
			position: absolute;
			width: 134px;
			height: 5px;
			left: calc(50% - 134px/2 + 0.5px);
			bottom: 8px;

			/* Label Color/Light/Primary */

			background: #000000;
			border-radius: 100px;
		}
	}
</style>