<script>
	import AboutLeftMountains from "../components/aboutLeftMountains.svelte";
	import AboutRightMountains from "../components/aboutRightMountains.svelte";
	import AboutMountain_1 from "../components/about_mountain_1.svelte";
</script>

<div style="position: relative; display: flex; justify-content: space-around;">
	<div class="text-container">
		<div class="about_title">About VH X</div>
		<div class="about_desc">
			Lorem Ipsum is simply dummy text of the printing and typesetting industry.
			Lorem Ipsum has been the industry's standard dummy text ever since the
			1500s, when an unknown printer took a galley of type and scrambled it to
			make a type specimen book.<br /><br />It has survived not only five
			centuries, but also the leap into electronic typesetting, remaining
			essentially unchanged. It was popularised in the 1960s with the release of
			<br /><br />Letraset sheets containing Lorem Ipsum passages, and more
			recently with desktop publishing software like Aldus PageMaker including
			versions of Lorem Ipsum.
		</div>
	</div>

	<div class="right-container">
		<div class="main-img-container mountain-img-container">
			<img src="/img/groupphoto.png" alt="group photo" />
			<div class="mountain1_svg">
				<AboutMountain_1 />
			</div>
		</div>
		<div class="miniature-container">
			<div class="mountain-img-container">
				<img
					src="/img/miniature1.png"
					class="miniature-img"
					alt="miniature 1"
				/>
				<div class="leftmountain_svg">
					<AboutLeftMountains />
				</div>
			</div>
			<div class="mountain-img-container">
				<img
					src="/img/miniature2.png"
					class="miniature-img"
					alt="miniature 2"
				/>
				<div class="rightmountain_svg">
					<AboutRightMountains />
				</div>
			</div>
		</div>
	</div>
</div>

<style>
	.text-container {
		flex: 1;
		max-width: calc(100% / 3);
		padding: 20px;
	}

	.about_title {
		color: #fff;
		text-shadow: 0px 0px 20px rgba(255, 255, 255, 0.73);
		font-family: Inter;
		font-size: 80px;
		font-style: normal;
		font-weight: 700;
		line-height: normal;
	}
	.about_desc {
		width: 504px;
		color: white;
		font-size: 20px;
		font-family: Inter;
		font-weight: 400;
		word-wrap: break-word;
	}

	/* Container styles */
	.mountain-img-container {
		position: relative;
		height: min-content;
	}

	.main-img-container img {
		width: 550px;
		object-fit: cover;
		z-index: 0;
	}

	.mountain1_svg {
		position: absolute;
		z-index: 1;
		bottom: -25px;
		width: 200px;
		left: -85px;
	}

	.leftmountain_svg {
		position: absolute;
		z-index: 1;
		bottom: -40px;
		width: 145px;
		left: -60px;
	}
	.rightmountain_svg {
		position: absolute;
		z-index: 1;
		bottom: -17px;
		width: 148px;
		right: -52px;
	}

	.right-container {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	.miniature-container {
		margin-top: 50px;
		display: flex;
		justify-content: space-around;
		width: 100%;
	}

	.miniature-img {
		width: 175px;
		object-fit: cover;
		border-radius: 50%;
	}

	@media only screen and (max-width: 768px) {
		.main-container {
			flex-direction: column;
			align-items: center;
		}
		.text-container {
			max-width: 100%;
			padding: 20px;
		}
		.about_desc {
			width: auto;
		}
		.right-container {
			align-items: center;
		}
		.miniature-container {
			flex-direction: column;
			align-items: center;
		}
		.main-img-container img {
			width: 100%;
		}
	}
</style>
