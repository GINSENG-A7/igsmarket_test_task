<template>
	<div class="bar">
		<div class="bar__items_left">
			<slot name="left"></slot>
		</div>
		<div class="bar__items_right">
			<slot name="right"></slot>
		</div>
	</div>
</template>

<script>
export default {
	name: "system-bar",
}
</script>

<style lang="scss" scoped>
	.bar {
		width: 100%;
		height: 44px;
		display: flex;
		align-items: center;
		flex-direction: row;
		justify-content: space-between;
		background: rgba(255, 255, 255, 0);
		// backdrop-filter: blur(26px);
		position: fixed;
		z-index: 2;
		top: 0;
		&__items_left {
			display: flex;
			align-items: center;
			flex-direction: row;
			margin: 2px 0 0 0;
			width: 50%;
			height: 22px;
			margin-left: 24px;
		}
		&__items_right {
			display: flex;
			align-items: center;
			flex-direction: row;
			margin: 2px 0 0 0;
			width: 50%;
			height: 22px;
			flex-flow: row-reverse;
			gap: 5.03px;
			margin-right: 14.67px;
		}
	}
</style>