<script>
	import { FaqItem, Button } from '$components';
	import twitterIcon from '$assets/icons/twitter.webp';

	const faqs = [
		{
			question: 'Why did the author move to Spain?',
			answer: 'The author was drawn to Spain’s rich culture, relaxed lifestyle, and sunny climate. What started as a short adventure turned into a long-term love affair with the country.'
		},
		{
			question: 'What was the hardest part about moving to Spain?',
			answer: 'Navigating the visa and residency process was one of the biggest challenges, closely followed by adjusting to the slower pace of bureaucracy and learning the language.'
		},
		{
			question: 'Is it easy to find work in Spain as a foreigner?',
			answer: 'It depends on your field and language skills. Teaching English, remote work, and tourism-related jobs are common options for expats, but the job market can be competitive.'
		},
		{
			question: 'What’s the biggest culture shock when moving to Spain?',
			answer: 'The concept of \'mañana\' — things often move at a slower pace than many newcomers are used to, especially when it comes to paperwork and customer service.'
		},
		{
			question: 'How important is it to speak Spanish when living in Spain?',
			answer: 'Speaking Spanish makes life significantly easier, especially when dealing with paperwork, local businesses, and building relationships with neighbors and locals.'
		},
		{
			question: 'What’s one thing the author wishes they knew before moving?',
			answer: 'That every region in Spain is incredibly different — from language and food to local customs. Understanding these differences can help you choose the best place to settle.'
		},
		{
			question: 'What’s the best part about living in Spain?',
			answer: 'The quality of life — affordable healthcare, a strong sense of community, beautiful landscapes, and the ability to enjoy life at a slower, more intentional pace.'
		},
		{
			question: 'Does the author plan to stay in Spain long-term?',
			answer: 'Absolutely! Spain feels like home now, and despite the initial challenges, the rewards have made it all worthwhile.'
		}
	];

	let questionCurrentlyExpanded = $state(-1);

	function onclick(index) {
		if (questionCurrentlyExpanded === index) {
			questionCurrentlyExpanded = -1;
		} else {
			questionCurrentlyExpanded = index;
		}
	}
</script>

<section class="main-section">
	<h2 class="mb-l">Frequently asked questions</h2>
	<div class="faq-container">
		{#each faqs as faq, index (faq.question)}
			<FaqItem {faq} isExpanded={index === questionCurrentlyExpanded} onclick={() => onclick(index)} />
		{/each}
	</div>
	<div class="additional-info mt-m">
		<Button class="mt-s">BUY NOW</Button>
		<p class="mt-m">Any other questions?</p>
		<a href="https://google.de">
			<p>Hit me up on Twitter <img src={twitterIcon} class="twitter-icon" alt="" /></p>
		</a>
	</div>
</section>

<style>
    .additional-info {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .twitter-icon {
        width: 18px;
        height: 18px;
    }

    a {
        text-decoration: underline;
    }
</style>