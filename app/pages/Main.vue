<template>
	<main id="main">
		<navigation></navigation>
		<section :style="{'background': style.background}">
			
		</section>
	</main>
</template>

<style lang="less" scoped>
</style>

<script>
	export default {
		mounted() {

		},

		computed: {
			style() {
				return this.$store.state.style;
			}
		}
	};
</script>
