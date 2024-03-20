<script lang="ts">
	import '../app.postcss';
	import { AppShell, AppBar } from '@skeletonlabs/skeleton';

	// Highlight JS
	import hljs from 'highlight.js/lib/core';
	import 'highlight.js/styles/github-dark.css';
	import { storeHighlightJs } from '@skeletonlabs/skeleton';
	import xml from 'highlight.js/lib/languages/xml'; // for HTML
	import css from 'highlight.js/lib/languages/css';
	import javascript from 'highlight.js/lib/languages/javascript';
	import typescript from 'highlight.js/lib/languages/typescript';

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
	let currentTile: number = 0;
</script>

<!-- App Shell -->
<AppShell>
	<svelte:fragment slot="header">
		<!-- App Bar -->
		<AppBar>
			<svelte:fragment slot="lead">
				<AppRailAnchor href="https://solaxium.com" target="_blank"
					><img class="solaxium-logo"
						style=
						"height:100px;
						 width:80px;
				    	 margin-left:-15px; 
						 margin-bottom:10px;
						 margin-top:-10px;" 
					src="/favicon.svg" alt="" /></AppRailAnchor
					>
				<img 
				style=
					"height:30px;
					margin-left:20px;
					" 
				src="/solaxium.svg" alt=""/>
			</svelte:fragment>
			<svelte:fragment slot="trail">
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://discord.gg/SxswvkgfKn"
					target="_blank"
					rel="noreferrer"
				>
					Discord
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://twitter.com/Solaxium"
					target="_blank"
					rel="noreferrer"
				>
					Twitter
				</a>
				<a
					class="btn btn-sm variant-ghost-surface"
					href="https://github.com/huncholane/solaxium"
					target="_blank"
					rel="noreferrer"
				>
					GitHub
				</a>
			</svelte:fragment>
		</AppBar>
	</svelte:fragment>
	<!-- Page Route Content -->
	<svelte:fragment slot="sidebarLeft">
		<AppRail>
			<svelte:fragment slot="lead">
				<AppRailAnchor href="https://github.com/huncholane/solaxium" target="_blank"
					><img style="margin:auto;" width="110%" src="/github.svg" alt="" /></AppRailAnchor
				>
			</svelte:fragment>
			<!-- --- -->
			<AppRailTile bind:group={currentTile} name="tile-1" value={0} title="tile-1">
				<svelte:fragment slot="lead">
					<AppRailAnchor href="https://discord.gg/SxswvkgfKn" target="_blank"
						><img style="margin:auto;" width="80%" src="/discord.svg" alt="" />
					</AppRailAnchor>
				</svelte:fragment>
			</AppRailTile>
			<AppRailTile bind:group={currentTile} name="tile-2" value={1} title="tile-2">
				<svelte:fragment slot="lead">
					<AppRailAnchor href="https://twitter.com/Solaxium" target="_blank">
						<div>
							<svg
								viewBox="0 0 24 24"
								aria-hidden="true"
								class="r-4qtqp9 r-yyyyoo r-dnmrzs r-bnwqim r-1plcrui r-lrvibr r-lrsllp r-1nao33i r-16y2uox r-8kz0gk"
								><g fill="white"
									><path
										d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"
									></path></g
								></svg
							><span
								class="css-1qaijid r-dnmrzs r-1udh08x r-3s2u2q r-bcqeeo r-qvutc0 r-poiln3 r-1inkyih r-rjixqe"
								style="text-overflow: unset;"
							></span>
						</div>
					</AppRailAnchor>
					<div dir="ltr" class="" style="text-overflow: unset; color: white; fill: white;"></div>
				</svelte:fragment>
			</AppRailTile>
			<AppRailTile bind:group={currentTile} name="tile-3" value={2} title="tile-3">
				<svelte:fragment slot="lead"
					><AppRailAnchor href="https://t.me/solaxium" target="_blank"
						><div>
							<img style="margin:auto;" width="80%" src="/telegram.svg" alt="" />
						</div></AppRailAnchor
					>
				</svelte:fragment>
			</AppRailTile>
			<!-- --- -->
			<svelte:fragment slot="trail">
				<AppRailAnchor href="/" target="_blank" title="Account">(Log Out)</AppRailAnchor>
			</svelte:fragment>
		</AppRail>
	</svelte:fragment>
	<slot />

	<svelte:fragment slot="footer">℗ Hygo AI & MonkeWifHat 2024</svelte:fragment>
</AppShell>
