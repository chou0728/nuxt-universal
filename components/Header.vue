<style scoped lang="scss">
.header {
	width: 100%;
	height: 80px;
	display: flex;
	justify-content: center;
	align-items: center;
	background: rgb(201, 192, 192);
}

.nav-items {
	width: 80%;
	list-style: none;
	padding: 0;
	margin: 0;
	display: flex;
	justify-content: space-around;
	align-items: center;
	text-decoration: none;
	color: #fff;

	a {
		text-decoration: none;
		color: #000;

		&:hover {
			color: #fff;
		}
	}
}
</style>

<template>
	<header class="header">
		<ul class="nav-items">
			<li>
				<nuxt-link to="/">Home</nuxt-link>
			</li>
			<li>
				<nuxt-link to="/users">Users</nuxt-link>
			</li>
		</ul>
	</header>
</template>
