<template>
	<div class="banner">
		<slot></slot>
	</div>
</template>

<script>
export default {
	name: 'personal-banner',
}
</script>

<style lang="scss" scoped>
	.banner {
		position: relative;
		// width: 100%;
		// height: 100%;
		text-align: center;
		vertical-align: middle;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
</style>