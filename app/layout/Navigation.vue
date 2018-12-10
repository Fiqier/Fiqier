<template>
	<nav class="Navigation">
		<div class="Navigation__left">
			<router-link to="/">Home</router-link>
			<router-link to="/drive">Drive</router-link>
			<router-link to="/search">Files</router-link>
			<router-link to="/tags">Tags</router-link>
		</div>

		<div class="Navigation__right">
			<omni-box></omni-box>
			<a class="Navigation__user Profile">
				<img class="Profile__image" :src="user.profileImage">
				<div class="Profile__content">
					<span class="Profile__name">
						{{user.name}}
					</span>
					<icon icon="chevron-down"></icon>
				</div>
			</a>
		</div>
	</nav>
</template>

<style lang="less" scoped>
	.Navigation {
		&__left {
			a {

			}
			
			a.router-link-active {

			}
		}

		&__right {
			flex: 1;
		}
	}
</style>

<script>
	export default {
		components: {
			Icon,
			OmniBox
		},

		computed: {
			user() {
				return this.$store.state.user;
			}
		}
	};
</script>
