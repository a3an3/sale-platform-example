<script>
	import phoneCover from '$assets/phone_cover.png';
	import bookCover from '$assets/book_cover.png';
	import { Button } from '$components/index.js';

	let { children } = $props();
</script>

<section class="hero">
	<div class="hero-showcase text-center bold">
		<h1 class="purple">MOVE TO</h1>
		<h1 class="purple mb-xs">SPAIN</h1>
		<h4 class="italic bold">There's no need to make the same mistakes I made</h4>
		<img class="book-cover" src={bookCover} alt="" />
		<img class="phone-cover" src={phoneCover} alt="" />
	</div>
	<div class="hero-text white text-center">
		{#if children}
			{@render children()}
		{:else}
			<h1>THIS EBOOK WILL</h1>
			<h1>SAVE YOU MONEY,</h1>
			<h1 class="mb-m">TIME & NERVES</h1>
			<p class="light-grey mb-l"> Seven years ago, I packed up my life and moved to Spain — and let me tell you, it
				wasn’t
				all sunshine and sangria. The process was far more painful than I expected, and I made every mistake in the book
				(plus a few I didn’t even know existed). But through all the stress, confusion, and cultural shocks, I gained
				invaluable insights that could make your move much smoother.
			</p>
			<Button>Purchase Now</Button>
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
        background: linear-gradient(
                135deg,
                #e2cbff,
                #e2cbff 25%,
                #deeaff 50%,
                #ece5ff 75%,
                #927bce
        );
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
        transform: translateY(20%);
    }

    .phone-cover {
        position: absolute;
        right: 52%;
        bottom: 100px;
        width: 35%;
        transform: translateY(30%);
    }


</style>