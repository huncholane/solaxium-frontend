<script>
	import LogoCloud from './LogoCloud.svelte';
</script>

<div class="row">
	<div class="copyright">
		<span>© Hygo AI & MonkeWifHat {new Date().getFullYear()}</span>
	</div>

	<LogoCloud />
</div>

<style>
	.row {
		display: flex;
		justify-content: space-between;
		padding-left: 10px;
		padding-right: 10px;
		padding-bottom: 10px;
		background-color: none;
	}
	span {
		margin: 0;
	}
	.copyright {
		display: flex;
		flex-direction: column;
		justify-content: end;
	}
</style>
