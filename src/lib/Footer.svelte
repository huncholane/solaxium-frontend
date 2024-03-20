<script>
	import LogoCloud from './LogoCloud.svelte';
</script>

<div class="row">
	<span>© Hygo AI & MonkeWifHat {new Date().getFullYear()}</span>
	<LogoCloud />
</div>

<style>
	.row {
		display: flex;
		justify-content: space-between;
		padding-left: 10px;
		padding-right: 10px;
	}
	span {
		margin: auto 0px;
	}
</style>
