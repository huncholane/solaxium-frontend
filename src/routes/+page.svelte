<script lang="typescript">
	import Roadmap from './../lib/Roadmap.svelte';
</script>

<div>
	<div class="container h-full mx-auto flex justify-center items-center">
		<div class="space-y-10 text-center flex flex-col items-center">
			<h2 class="h2">Welcome to the Solaxium Ecosystem.</h2>
			<!-- Animated Logo -->
			<img src="/favicon.svg" width="200px" alt="" />
			<!-- / -->
			<div class="flex justify-center space-x-2">
				<a class="btn variant-filled" href="https://t.me/solaxium" target="_blank" rel="noreferrer">
					Join the Ecosystem
				</a>
			</div>
			<div class="space-y-2"></div>
		</div>
	</div>
	<Roadmap />
</div>

<style lang="postcss">
	figure {
		@apply flex relative flex-col;
	}
	figure svg,
	.img-bg {
		@apply w-64 h-64 md:w-80 md:h-80;
	}
	.img-bg {
		@apply absolute z-[-1] rounded-full blur-[50px] transition-all;
		animation:
			pulse 5s cubic-bezier(0, 0, 0, 0.5) infinite,
			glow 5s linear infinite;
	}
	@keyframes glow {
		0% {
			@apply bg-primary-400/50;
		}
		33% {
			@apply bg-secondary-400/50;
		}
		66% {
			@apply bg-tertiary-400/50;
		}
		100% {
			@apply bg-primary-400/50;
		}
	}
	@keyframes pulse {
		50% {
			transform: scale(1.5);
		}
	}
</style>
