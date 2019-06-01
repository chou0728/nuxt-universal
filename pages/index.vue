<style scoped lang="scss">
.container {
	margin: 0 auto;
	min-height: 50vh;
	display: flex;
	justify-content: center;
	align-items: center;
	text-align: center;
}

.link-item {
	display: inline-block;
	margin: 20px;
	color:$deep-blue;
}
</style>

<template>
	<div>
		<section class="container">
			<div>
				<!-- 會創造全新的一頁，跳脫SPA，並對server發出新的request，css樣式也不會吃到SPA全域的樣式 -->
				<a class="link-item" href="/users">Users</a>
				<br>
				<!--原有的SPA下去做routing，底層使用vue router -->
				<nuxt-link class="link-item" to="/users">Users(nuxt-link)</nuxt-link>
				<br>
				<button class="link-item" @click="$router.push('/products')">Go to Products Page</button>
			</div>
		</section>
	</div>
</template>

