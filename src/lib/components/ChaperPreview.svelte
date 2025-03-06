<script>
	const chapters = [
		{
			number: 1,
			title: 'The Spanish Bureaucracy',
			strapline: 'Understanding Visas, Residency, and Legal Essentials',
			excerpt: 'Moving to Spain involves navigating a labyrinth of bureaucratic processes that can feel overwhelming at first. This chapter breaks down visas, residency permits, and essential legal steps to help you start your journey with confidence.'
		},
		{
			number: 2,
			title: 'Finding Your Dream Home in Spain',
			strapline: 'From Coastal Villas to Urban Apartments: Where and How to Live',
			excerpt: 'Spain offers a diverse array of living options, from picturesque coastal towns to bustling city centers. This chapter guides you through house-hunting, rental contracts, and buying property in Spain.'
		},
		{
			number: 3,
			title: 'Mastering the Spanish Job Market',
			strapline: 'Strategies for Employment and Freelancing in a New Culture',
			excerpt: 'Finding a job in Spain can be a challenging but rewarding experience, especially if you\'re not familiar with local hiring customs. This chapter offers practical tips for job seekers and freelancers navigating the Spanish job market.'
		},
		{
			number: 4,
			title: 'Embracing the Spanish Lifestyle',
			strapline: 'Cultural Norms, Social Etiquette, and Making New Connections',
			excerpt: 'Moving to Spain isn’t just about changing your location; it’s about immersing yourself in a new way of life. This chapter explores cultural norms, social customs, and how to build friendships in your new home.'
		},
		{
			number: 5,
			title: 'Overcoming the Language Barrier',
			strapline: 'Learning Spanish for Everyday Life',
			excerpt: 'Whether you arrive with basic Spanish or none at all, learning the language is key to thriving in Spain. This chapter covers practical language-learning tips, common phrases, and strategies for boosting your confidence in conversations.'
		}
	];

	let selectedChapterNumber = $state(1);
	let selectedChapter = $derived(chapters.find(chapter => chapter.number === selectedChapterNumber));

	function selectChapter(chapter) {
		selectedChapterNumber = chapter.number;
	}
</script>

<section class="main-section default-margin">
	<h2 class="mb-l">What you're getting</h2>
	<div class="chapter-container">
		<ul>
			{#each chapters as chapter (chapter.number)}
				<li>
					<button
						class="chapter-title"
						class:selected-chapter-title={selectedChapterNumber === chapter.number}
						aria-controls={`chapter-info-${chapter.number}`}
						onclick={() => selectChapter(chapter)}
						aria-expanded={selectedChapterNumber === chapter.number}>
						<h4>Chapter {chapter.number}: {chapter.title}</h4>
					</button>
				</li>

			{/each}
		</ul>
		<div class="chapter-info">
			<h3 class="chapter-strapline italic mb-s">{selectedChapter.title}</h3>
			<p>{selectedChapter.excerpt}</p>
		</div>
	</div>
</section>

<style>
    .chapter-container {
        display: flex;
        justify-content: space-between;
    }

    .chapter-container ul {
        width: 40%;
    }

    .chapter-info {
        width: 55%;
    }

    .chapter-title {
        border-bottom: 1px solid grey;
        width: 100%;
        display: block;
        padding: 12px;
        text-align: left;
    }

    .selected-chapter-title {
        background-color: black;
        border: none;
        color: white;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1),
        0 1px 3px rgba(0, 0, 0, 0.08);
    }
</style>