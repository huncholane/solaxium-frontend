<script>
	import Icon from '@iconify/svelte';
</script>

<footer class="footer">
	<div class="container">
		<div class="row">
			<div class="footer-col">
				<h4>Email</h4>
				<ul>
					<li>
						<a style="text-transform: none;" href="mailto:team@solaxium.com" target="_blank"
							>team@solaxium.com</a
						>
					</li>
				</ul>
			</div>
			<div class="footer-col">
				<h4>Partners</h4>
				<ul>
					<li><a href="https://hygo.ai">Hygo AI</a></li>
					<li><a href="https://monkewifhat.com" target="_blank">MonkeWifHat ($MIF)</a></li>
				</ul>
			</div>

			<div class="footer-col">
				<h4>follow us</h4>
				<div class="social-links">
					<a class="logo-item p-2" href="https://twitter.com/Solaxium" target="_blank">
						<div class="logo-container">
							<span><Icon icon="tabler:brand-x" width="32px" /></span>
						</div>
					</a>
					<a class="logo-item p-2" href="https://t.me/solaxium" target="_blank">
						<div class="logo-container">
							<span><Icon icon="tabler:brand-telegram" width="32px" /></span>
						</div>
					</a>
					<a class="logo-item p-2" href="https://github.com/huncholane/solaxium" target="_blank">
						<div class="logo-container">
							<span><Icon icon="tabler:brand-github-filled" width="32px" /></span>
						</div>
					</a>
					<a class="logo-item p-2" href="https://discord.gg/SxswvkgfKn" target="_blank">
						<div class="logo-container">
							<span><Icon icon="tabler:brand-discord-filled" width="32px" /></span>
						</div>
					</a>
				</div>
			</div>
		</div>
	</div>
</footer>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap');
	body {
		line-height: 1.5;
		font-family: 'Poppins', sans-serif;
	}
	* {
		margin: 0;
		padding: 0;
		box-sizing: border-box;
	}
	.container {
		max-width: 1170px;
		margin: auto;
	}
	.row {
		display: flex;
		flex-wrap: wrap;
	}
	ul {
		list-style: none;
	}
	.footer {
		padding: 90px 0 60px 0;
	}
	.footer-col {
		width: 25%;
		padding: 0 15px;
	}
	.footer-col h4 {
		font-size: 18px;
		color: #ffffff;
		text-transform: capitalize;
		margin-bottom: 35px;
		font-weight: 500;
		position: relative;
	}
	.footer-col h4::before {
		content: '';
		position: absolute;
		left: 0;
		bottom: -10px;
		background-color: #e91e63;
		height: 2px;
		box-sizing: border-box;
		width: 50px;
	}
	.footer-col ul li:not(:last-child) {
		margin-bottom: 10px;
	}
	.footer-col ul li a {
		font-size: 16px;
		text-transform: capitalize;
		color: #ffffff;
		text-decoration: none;
		font-weight: 300;
		color: #bbbbbb;
		display: block;
		transition: all 0.3s ease;
	}
	.footer-col ul li a:hover {
		color: #ffffff;
		padding-left: 8px;
	}
	.footer-col .social-links a {
		display: inline-block;
		height: 40px;
		width: 40px;
		background-color: rgba(255, 255, 255, 0.2);
		margin: 0 10px 10px 0;
		text-align: center;
		line-height: 40px;
		border-radius: 50%;
		color: #ffffff;
		transition: all 0.5s ease;
	}
	.footer-col .social-links a:hover {
		color: #24262b;
		background-color: #ffffff;
	}

	/*responsive*/
	@media (max-width: 767px) {
		.footer-col {
			width: 50%;
			margin-bottom: 30px;
		}
	}
	@media (max-width: 574px) {
		.footer-col {
			width: 100%;
		}
	}

	.logo-container {
		display: flex;
		justify-content: center;
		margin-top: 4px;
	}
	.logo-container span {
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
</style>
