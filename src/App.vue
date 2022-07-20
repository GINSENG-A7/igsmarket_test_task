<template>
	<div class="app_container">
		<div class="transition__block">
			<system-bar>
				<template #left>
					<div class="time" v-for="smil in systemMenuItemsLeft" :key="smil.id">{{smil.text}}</div>
				</template>
				<template #right>
					<div class="imageWrapper" v-for="smir in systemMenuItemsRight" :key="smir.id">
						<img :src="smir.picturePath">
					</div>
				</template>
			</system-bar>
	
			<custom-header class="custom__header">
				<template #topic>
					<p id="topic_p">Мой ИЖС</p>
				</template>
				<template #letter>
					{{this.user.login.toUpperCase().substring(0,1)}}
				</template>
				<template #state>
					<p id="state_p">cтатус</p>
				</template>
			</custom-header>
		</div>

		<div class="offer__cell">
			<div class="flex_container">
				<div class="text">
					{{this.offer}}
				</div>
				<personal-banner class="big__banner">
					{{this.user.login.toUpperCase().substring(0,1)}}
				</personal-banner>
			</div>
		</div>
		<menu-list class="menu-list" :menuItems="menuItems"></menu-list>
		<nav-bar class="nav-bar" :navBarItems="navBarItems"></nav-bar>
	</div>
</template>

<script>
export default {
	name: 'App',
	data() {
		return {
			systemMenuItemsLeft: [
				{id: 1,	text: "9:41"},
			],
			systemMenuItemsRight: [
				{id: 1, picturePath: require('./assets/Battery.png')},
				{id: 2, picturePath: require('./assets/Wifi.png')},
				{id: 3, picturePath: require('./assets/MobileSignal.png')},
			],
			user: {
				id: 1,
				login: "Ginseng",
			},
			offer: "Все инженеры и Росреестр за 0 ₽ — оплатите первый этап строительства до 25 августа и Genius активируется автоматически",
			menuItems: [
				{id: 1, title: "Как это работает", iconPath: require('./assets/menu_icons_32px.png')},
				{id: 2, title: "ИЖС Стандарт", iconPath: require('./assets/menu_icons_32px(1).png')},
				{id: 3, title: "Договоры", iconPath: require('./assets/menu_icons_32px(2).png')},
				{id: 4, title: "Росреестр", iconPath: require('./assets/menu_icons_32px(3).png')},
				{id: 5, title: "Помощь", iconPath: require('./assets/menu_icons_32px(4).png')},
				{id: 6, title: "Промокоды", iconPath: require('./assets/menu_icons_32px(5).png')},
				{id: 7, title: "Партнёрам", iconPath: require('./assets/menu_icons_32px(6).png')},
				{id: 8, title: "Избранное", iconPath: require('./assets/menu_icons_32px(7).png')},
			],
			navBarItems: [
				{id: 1, title: "Главная", iconPath: require('./assets/Frame.png')},
				{id: 2, title: "Каталог", iconPath: require('./assets/Frame(1).png')},
				{id: 3, title: "Landscape", iconPath: require('./assets/Frame(2).png')},
				{id: 4, title: "Стройка", iconPath: require('./assets/Frame(3).png')},
				{id: 5, title: "Меню", iconPath: require('./assets/Frame(4).png')},
			],
		}
	},
}
</script>

<style lang="scss">
body {
	font-family: 'Roboto Flex';
	text-align: center;
	margin: 0;
	p {
		margin: 0;
		align-content: center;
		vertical-align: middle;
	}
	.small__banner {
		width: 24px;
		height: 24px;
		margin: 4px;
		background: linear-gradient(90deg, #C5ACFF 0%, #FBC2EB 100%);
		border-radius: 24px;
	}
	.big__banner {
		min-width: 64px;
		min-height: 64px;
		background: linear-gradient(90deg, #C5ACFF 0%, #FBC2EB 100%);
		border-radius: 10px;
		font-size: 50px;
		font-weight: 1000;
	}
}
.app_container {
	width: 100%;
	.transition__block {
		position: fixed;
		width: 100%;
		height: 92px;
		backdrop-filter: blur(26px);
		z-index: 1;
		margin-top: -116px;
		background: rgba(245, 245, 245, 0.94);
	}
	.time {
		width: 54px;
		font-style: normal;
		font-weight: 750;
		font-size: 14px;
		line-height: 20px;
		text-align: center;
		letter-spacing: -0.5px;
		color: #000000;
	}
	.imageWrapper {

	}
	.custom__header {
		#topic_p {
			width: 147px;
			height: 31px;
			font-size: 26px;
		}
		#letter_p {
			// position: absolute;
			// left: 28.57%;
			// right: 28.57%;
			// top: 28.57%;
			// bottom: 28.57%;\
			width: 100%;
			height: fit-content;
			vertical-align: middle;

		}
		#state_p {
			width: 56px;
			height: 17px;
			font-size: 14px;
		}
	}
	.offer__cell{
		margin: 116px auto 0 auto;
		width: 89.5%;
		height: fit-content;
		background: #090909;
		border-radius: 16px;
		.flex_container {
			padding: 16px;
			display: flex;
			flex-direction: row;
			justify-content: space-between;
			align-items: flex-start;
			gap: 16px;
			.text {
				text-align: left;
				width: auto;
				height: 100%;
				font-family: 'Roboto Flex';
				font-style: normal;
				font-weight: 750;
				font-size: 12px;
				line-height: 125%;
				color: #F9F9F9;
			}
		}
	}
	.menu-list {
		margin-bottom: 100px;
	}
	.nav-bar {

	}
}
</style>
