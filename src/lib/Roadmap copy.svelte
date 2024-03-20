<div class="timeline-area">
	<div class="container">
		<div class="timelines">
			<h2>Timelines</h2>
		</div>
		<div class="all-timelines">
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>March 2024</h6>
						— Launch of dev team community token $MIF.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>March 2024</h6>
						— Partnerships and connections aquired through $MIF.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>March 2024</h6>
						— Javascript prototype.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>April 2024</h6>
						— Backend Rust Solana exchange solutions.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>May 2024</h6>
						— Token launch, staking enabled.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>June 2024</h6>
						— Beta testing and partnership building.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
			<!--SINGLE TIMELINE-->
			<div class="single-timeline d-flex-2">
				<div class="timeline-blank"></div>
				<div class="timeline-text d-flex-2">
					<span>
						<h6>September 2024</h6>
						— Public usage for Solaxium.
					</span>
					<div class="t-square"></div>
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	* {
		margin: 0;
		padding: 0;
	}

	body {
		background-color: #1d2123;
		font-family: 'Inter', sans-serif;
	}

	ul {
		list-style: none;
		margin: 0 !important;
	}

	a {
		text-decoration: none !important;
		display: inline-block;
	}

	img {
		max-width: 100%;
	}

	button:focus {
		outline: none;
	}

	h1,
	h2,
	h3,
	h4,
	h5,
	h6 {
		margin: 0;
	}
	p {
		font-size: 14px;
		line-height: 26px;
		margin: 0;
	}
	.container {
		width: 100%;
		max-width: 1140px;
		padding: 0 15px;
		box-sizing: border-box;
		margin: 0 auto;
	}
	.timelines h2 {
		text-align: center;
		color: #fff;
		font-weight: 600;
		margin-bottom: 40px;
		font-size: 32px;
	}
	.d-flex-2 {
		display: flex;
		align-items: center;
	}
	.timeline-area {
		padding: 80px 0;
	}
	.all-timelines {
		position: relative;
	}
	.timelines h2 {
		text-align: center;
		color: #fff;
		font-weight: 600;
		margin-bottom: 40px;
	}
	.all-timelines::before {
		content: '';
		position: absolute;
		left: 0;
		right: 0;
		margin: auto;
		height: 100%;
		width: 2px;
		background: #efa22f;
		top: 20px;
	}
	.single-timeline {
		margin-bottom: 22px;
	}
	.timeline-blank {
		width: 50%;
	}
	.timeline-text {
		width: 50%;
		padding-left: 30px;
		-webkit-box-sizing: border-box;
		box-sizing: border-box;
		position: relative;
	}
	.timeline-text h6 {
		color: #f0f1f2;
		font-weight: 900;
		display: inline-block;
		font-size: 1rem;
	}
	.timeline-text span {
		color: #f0f1f2;
		display: block;
		width: 100%;
	}
	.single-timeline:nth-child(even) .timeline-text span {
		text-align: right;
	}
	.t-square {
		content: '';
		position: absolute;
		width: 12px;
		height: 12px;
		left: -6px;
		background: #efa22f;
	}
	.single-timeline:nth-child(even) {
		-webkit-box-orient: horizontal;
		-webkit-box-direction: reverse;
		-ms-flex-direction: row-reverse;
		flex-direction: row-reverse;
	}
	.single-timeline:nth-child(even) .t-square {
		right: -6px;
		left: unset;
	}
	.single-timeline:nth-child(even) .timeline-text {
		padding-left: 0;
		padding-right: 30px;
		text-align: right;
	}

	@media all and (max-width: 991px) {
	}
	@media all and (max-width: 768px) {
		.all-timelines::before {
			right: unset;
			top: 0;
		}
		.single-timeline:nth-child(2n) .timeline-text {
			padding-left: 30px;
			padding-right: 0;
			text-align: left;
		}
		.single-timeline:nth-child(2n) .t-square {
			left: -6px;
			right: unset;
		}
		.timeline-blank {
			display: none;
		}
		.timeline-text {
			width: 100%;
		}
		.single-timeline:nth-child(even) .timeline-text span {
			text-align: left !important;
		}
	}
	@media all and (max-width: 575px) {
	}
	@media all and (max-width: 360px) {
		.all-timelines::before {
			top: 32px;
		}
	}
</style>
