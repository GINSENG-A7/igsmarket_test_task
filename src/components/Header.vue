<template>
	<div class="header">
		<div class="flex__container">
			<div class="label">
				<slot name="topic"></slot>
			</div>
			<div class="info">
				<personal-banner class="small__banner">
					<slot name="letter"></slot>
				</personal-banner>
				<slot name="state"></slot>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	name: "custom-header",
}
</script>
PersonalBanner

<style lang="scss" scoped>
	.header {
		background: rgba(255, 255, 255, 0);
		height: 48px;
		width: 100%;
		font-family: 'Roboto Flex';
		font-style: normal;
		font-weight: 750;
		color: #090909;
		// backdrop-filter: blur(26px);
		position: fixed;
		z-index: 2;
		top: 43px;
		.flex__container {
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: center;
			padding: 8px 16px 8px 16px;
			.label {
				width: 147px;
				height: 31px;
			}
			.info {
				width: 92px;
				height: 32px;
				display: flex;
				flex-direction: row;
				justify-content: space-between;
				align-items: center;
				flex-flow: row;
			}
		}
	}
</style>