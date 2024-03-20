<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar, type ConicStop, ConicGradient } from '@skeletonlabs/skeleton';

	// Highlight JS
	import hljs from 'highlight.js/lib/core';
	import 'highlight.js/styles/github-dark.css';
	import { storeHighlightJs } from '@skeletonlabs/skeleton';
	import xml from 'highlight.js/lib/languages/xml'; // for HTML
	import css from 'highlight.js/lib/languages/css';
	import javascript from 'highlight.js/lib/languages/javascript';
	import typescript from 'highlight.js/lib/languages/typescript';
	import Icon from '@iconify/svelte';

	hljs.registerLanguage('xml', xml); // for HTML
	hljs.registerLanguage('css', css);
	hljs.registerLanguage('javascript', javascript);
	hljs.registerLanguage('typescript', typescript);
	storeHighlightJs.set(hljs);

	// Floating UI for Popups
	import { computePosition, autoUpdate, flip, shift, offset, arrow } from '@floating-ui/dom';
	import { storePopup } from '@skeletonlabs/skeleton';
	storePopup.set({ computePosition, autoUpdate, flip, shift, offset, arrow });

	//Popout Menu
	import { AppRail, AppRailTile, AppRailAnchor } from '@skeletonlabs/skeleton';
	import LogoCloud from '$lib/LogoCloud.svelte';
	import Footer from '$lib/Footer.svelte';
	import SocialBar from '$lib/SocialBar.svelte';
	let currentTile: number = 0;
</script>

<svelte:head>
	<title>Solaxium</title>
	<link rel="icon" type="image/png" href="/favicon.svg" />
	<meta
		name="description"
		content="The upgrade Solana needs. Upgrade to the current Solana dex platforms and coding experience."
	/>

	<!-- Facebook Meta Tags -->
	<meta property="og:url" content="https://solaxium.com" />
	<meta property="og:type" content="website" />
	<meta property="og:title" content="" />
	<meta
		property="og:description"
		content="The upgrade Solana needs. Upgrade to the current Solana dex platforms and coding experience."
	/>
	<meta
		property="og:image"
		content="https://opengraph.b-cdn.net/production/documents/be2ed16c-b994-4492-a3ca-677b03ae7f30.jpg?token=nHWBG84EZhX7fPIeJJ-SqNdYxMCl1p8rGjGFLgmnOSs&height=1024&width=1024&expires=33246948311"
	/>

	<!-- Twitter Meta Tags -->
	<meta name="twitter:card" content="summary_large_image" />
	<meta property="twitter:domain" content="solaxium.com" />
	<meta property="twitter:url" content="https://solaxium.com" />
	<meta name="twitter:title" content="" />
	<meta
		name="twitter:description"
		content="The upgrade Solana needs. Upgrade to the current Solana dex platforms and coding experience."
	/>
	<meta
		name="twitter:image"
		content="https://opengraph.b-cdn.net/production/documents/be2ed16c-b994-4492-a3ca-677b03ae7f30.jpg?token=nHWBG84EZhX7fPIeJJ-SqNdYxMCl1p8rGjGFLgmnOSs&height=1024&width=1024&expires=33246948311"
	/>
</svelte:head>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<AppRailAnchor href="/" target="_blank"
					><img class="solaxium-brand" src="/favicon.svg" alt="" /></AppRailAnchor
				>
				<img class="solaxium-logo" src="/solaxium.svg" alt="" />
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->

	<slot />
</AppShell>

<style>
	.solaxium-brand {
		width: 300px;
		height: 250px;
		margin-left: -60px;
		margin-bottom: -100px;
		margin-top: -100px;
	
	}
	.solaxium-logo {
		width: 450px;
		height: 100px;
		margin-left: -80px;
		margin-top: 30px;
		margin-bottom: -25px;
		
		
	}
	h1 {
		font-size: 30px;
		padding-bottom: 15px;
	}
</style>
