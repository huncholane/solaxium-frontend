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
			<svelte:fragment slot="trail">
				<div style="display: flex; flex-direction: row;">
					<a
						class="btn btn-sm variant-ghost-surface"
						href="https://github.com/huncholane/solaxium/blob/main/ReadMe.md"
						target="_blank"
						rel="noreferrer"
					>
						WhitePaper
					</a>
				</div>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->

	<slot />
</AppShell>

<style>
	.solaxium-brand {
		width: 90px;
		margin-left: -10px;
	}
	.solaxium-logo {
		width: 180px;
	}
</style>
