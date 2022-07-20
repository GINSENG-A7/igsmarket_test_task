<template>
	<div class="menu">
		<menu-item v-for="menuItem in menuItems" :menuItem="menuItem" :key="menuItem.id"></menu-item>
	</div>
</template>

<script>
export default {
	name: "menu-list",
	props: {
		menuItems: {
			type: Array,
			required: true,
		}
	}
}
</script>

<style>
	.menu{
		margin: 24px auto 0 auto;
		width: 89.5%;
		height: fit-content;
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		padding: 0px;

	}
</style>