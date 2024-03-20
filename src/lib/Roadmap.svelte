<script>
	import { Step, Stepper } from '@skeletonlabs/skeleton';
</script>

<div>
	<Stepper>
		<Step>
			<svelte:fragment slot="header">March 2024</svelte:fragment>
			Launch of dev team community token <a href="https://monkewifhat.com">monkewifhat ($MIF)</a>.
		</Step>
		<Step>
			<svelte:fragment slot="header">March 2024</svelte:fragment>
			Partnerships and connections aquired through $MIF.
		</Step>
		<Step>
			<svelte:fragment slot="header">March 2024</svelte:fragment>
			Javascript prototype for automated Solana bots.
		</Step>
		<Step>
			<svelte:fragment slot="header">April 2024</svelte:fragment>
			Backend Rust Solana exchange solutions.
		</Step>
		<Step>
			<svelte:fragment slot="header">May 2024</svelte:fragment>
			Token launch, staking enabled.
		</Step>
		<Step>
			<svelte:fragment slot="header">June 2024</svelte:fragment>
			Beta testing and partnership building.
		</Step>
		<Step>
			<svelte:fragment slot="header">September 2024</svelte:fragment>
			Public usage for Solaxium.
		</Step>
	</Stepper>
</div>

<style>
	div {
		width: 80%;
		margin: auto;
	}
	a {
		color: #d1548d;
	}
</style>
