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
						Solana paved the foundation for a truly great market, however the dex platforms cause issues when
						placing orders & the available platforms are slow and buggy.
					</li>
					<li>
						The Solana Web3 SDKS don't offer much help when the documentation for it is severely outdated, especially when it comes to making efficient
						Solana automations. Right now it's difficult to, and sometimes impossible to track transactions on
						the JavaScript SDK.
					</li>
					<li>
						The Rust SDK works much better out of the box, but the documentation lacks the robust support some chains boast and that creates
						many complexities, especially for new developers.
					</li>
				</ol>
			{:else if tabSet === 1}
				<ol>
					<li>
						When a user interfaces with either the Jupiter or Raydium exchanges, there is a good chance the they will run into
						bugs in the offset if their user experiences. This leads to failed trades and poor visualization of profit and loss margins.
					</li>
					<li>
						Earlier this year, we launched our community token MonkeWifHat ($MIF) and ran into many difficulties interacting
						with the Raydium AMM generator. We knew then we had to switch to a new platform, but which one?
						With no solution easily available, we set out to make our own.
					</li>
					<li>
						We enjoy the Bonk Telegram Trading bot as it simplifies the process of placing orders on the Raydium
						exchange, and speeds up the rate at which information is available to its users. Shout out to the Bonk devs largely inspriring this project.
					</li>
				</ol>
			{:else if tabSet === 2}
				<ol>
					<li>Finally! Solaxium, the fastest de-centralized, Solana-based, utility-driven exchange is here to simplify trading with a much more efficient solution!</li>
					<li>
					 	We all know how inefficient JavaScript is (Devs that is), especially for something as big, scalable, and publiclly available
						as Solana. We say no more!
					</li>
					<li>
						Our team will create an efficient and simplified Rust library to replace the clunky, old Solana CLI and use it to build both an exchange platform
						and lightning-fast utilities.
						"What's next then?", you ask? Wouldn't you like to know? 
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
