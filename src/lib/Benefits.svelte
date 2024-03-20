<script>
	import Icon from '@iconify/svelte';
	import { Tab, TabGroup } from '@skeletonlabs/skeleton';

	let tabSet = 0;
</script>

<div>
	<h1>Why Solaxium?</h1>
	<TabGroup>
		<Tab bind:group={tabSet} name="tab1" value={0}>
			<svelte:fragment slot="lead"
				><div class="icon-container">
					<Icon icon="tabler:alert-square-rounded" width="48" />
				</div></svelte:fragment
			>
			<span>The Issue</span>
		</Tab>
		<Tab bind:group={tabSet} name="tab2" value={1}>
			<svelte:fragment slot="lead"
				><div class="icon-container">
					<Icon icon="tabler:notes" width="48" />
				</div></svelte:fragment
			>
			Case Studies</Tab
		>
		<Tab bind:group={tabSet} name="tab3" value={2}>
			<svelte:fragment slot="lead"
				><div class="icon-container">
					<Icon icon="tabler:flask" width="48" />
				</div></svelte:fragment
			>
			Solution</Tab
		>
		<!-- Tab Panels --->
		<svelte:fragment slot="panel">
			{#if tabSet === 0}
				<ol>
					<li>
						Solana has the foundation to be truly great, however the dex platforms cause issues when
						placing orders effectively. The available platforms are slow and buggy.
					</li>
					<li>
						The Solana web3 sdks don't help very much, especially when it comes to making efficient
						Solana automations. It's difficult to and sometimes impossible to track transactions on
						the javascript SDK.
					</li>
					<li>
						The Rust sdk works much better, but the documentation lacks many examples and creates
						large complexities, especially for new developers.
					</li>
				</ol>
			{:else if tabSet === 1}
				<ol>
					<li>
						When one interacts with Jupiter or Raydium there is a good chance the user will run into
						bugs in the first 30 seconds.
					</li>
					<li>
						We launched our community token monkewifhat ($MIF) and ran into difficulties interacting
						with the Raydium AMM generator. We had to switch to a new platform.
					</li>
					<li>
						We enjoy the Bonk bot as it simplifies the process of placing orders on the Raydium
						exchange. Shout out to the Bonk devs for the inspiration of Sollaxium.
					</li>
				</ol>
			{:else if tabSet === 2}
				<ol>
					<li>Sollaxium is here to simplify trading with a much more efficient solution.</li>
					<li>
						Our team wants to write a backend in the efficient language Rust, which is what Solana
						is based on. We all know how inefficient JavaScript is, especially for something as big
						as Solana.
					</li>
					<li>
						We will create a simplified Rust cli and grow it over time towards a web user interface.
						Our plans on how to do so will remain private to the Sollaxium company.
					</li>
				</ol>
			{/if}
		</svelte:fragment>
	</TabGroup>
</div>

<style>
	div {
		margin: 70px 10% 140px 10%;
	}
	h1 {
		font-size: 30px;
		padding-bottom: 20px;
	}
	ol {
		list-style-type: decimal;
		margin-left: 20px;
	}
	.icon-container {
		display: flex;
		justify-content: center;
		margin: 0;
	}
</style>
