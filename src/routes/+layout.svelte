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
				<img style="margin-left:0%;" width="10%" src="/solaxiumlogo.webp" alt="" />
				<strong class="text-xl uppercase">Solaxium</strong>
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
						</AppRailAnchor
					>
				</svelte:fragment>
			</AppRailTile>
			<AppRailTile bind:group={currentTile} name="tile-2" value={1} title="tile-2">
				<svelte:fragment slot="lead">
					<AppRailAnchor href="https://twitter.com/Solaxium" target="_blank">
						<div>
							<img style="margin:auto;" width="80%" src="/x.svg" alt="" />
						</div>
							</AppRailAnchor>
							<div
								dir="ltr"
								class=""
								style="text-overflow: unset; color: white; fill: white;">
							</div>
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
