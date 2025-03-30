<script>
	import BookCover from '$assets/book_cover.png';
	import PhoneCover from '$assets/phone_cover.png';
	import { Button } from '$components';

	let { children } = $props();
</script>

<section class="hero">
	<div class="hero-showcase text-center bold">
		<h1 class="purple">MOVE TO</h1>
		<h1 class="purple mb-xs">SPAIN</h1>
		<h4 class="italic semi-bolöd">There's no need to make the same mistakes I made.</h4>
		<img class="book-cover" src={BookCover} alt="" draggable="false" />
		<img class="phone-cover" src={PhoneCover} alt="" draggable="false" />
	</div>
	<div class="hero-text white text-center">
		{#if children}
			{@render children()}
		{:else}
			<h1>THIS EBOOK WILL</h1>
			<h1>SAVE YOU MONEY,</h1>
			<h1 class="mb-m">TIME & NERVES</h1>
			<p class="light-grey mb-l">
				Lorem ipsum dolor sit amet consectetur adipisicing elit. Temporibus recusandae voluptatum
				qui eum vitae, consectetur illo voluptate iure quis eligendi commodi perferendis vel ea
				distinctio consequatur pariatur cumque suscipit eveniet?
			</p>
			<Button>Purchase E-book for $10</Button>
		{/if}
	</div>
</section>

<style>
	.hero {
		display: flex;
		height: 100vh;
		overflow-y: hidden;
	}

	.hero-showcase {
		position: relative;
		width: 50%;
		padding: 100px 16px 0 16px;
		background: linear-gradient(135deg, #e2cbff, #e2cbff 25%, #deeaff 50%, #ece5ff 75%, #927bce);
	}

	.hero-text {
		padding: 100px 5%;
		width: 50%;
		background-color: black;
	}

	.book-cover {
		position: absolute;
		right: 2%;
		bottom: 0;
		width: 65%;
		transform: translateY(30%);
	}

	.phone-cover {
		position: absolute;
		width: 35%;
		bottom: 0;
		right: 52%;
		transform: translateY(25%);
	}
</style>
