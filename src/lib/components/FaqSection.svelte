<script>
	import { FaqItem, Button } from '$components';
	import twitterIcon from '$assets/icons/twitter.webp';
</script>

<section class="main-section">
	<h2 class="mb-l">Frequently asked questions</h2>
	<div class="faq-container">
		<FaqItem />
	</div>
	<div class="additional-info">
		<Button class="mt-s">BUY NOW</Button>
		<p class="mt-m">Any other questions?</p>
		<a href="https://google.de">
			<p>Hit me u on Twitter <img src={twitterIcon} class="twitter-icon" alt="" /></p>
		</a>
	</div>
</section>

<style>

</style>