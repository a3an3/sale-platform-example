<script>
	import authorPic from '$assets/author_pic.png';
</script>


<section class="author-section">
	<h2 class="mb-l">About the Author</h2>
	<div class="author-container">
		<div class="author-text">
			<p class="mb-xs">
				The author is an experienced expatriate who moved to Spain seven years ago and navigated the challenges of
				starting a new life in a foreign country. Through firsthand experience, they have gained deep insights into
				Spain’s bureaucracy, culture, and way of life. With a passion for sharing knowledge, they provide practical
				advice, personal anecdotes, and essential tips for anyone considering a move to Spain. Their writing aims to
				simplify complex processes, offer cultural guidance, and help newcomers transition smoothly into Spanish life.
				Whether it’s dealing with visas, finding a home, or embracing the local lifestyle, the author’s expertise is a
				valuable resource for future expats.
			</p>
			<p>
				Whether you’re planning a short-term adventure or a permanent relocation, the author’s experiences provide
				valuable lessons and a reassuring reminder that with patience, preparation, and an open mind, starting fresh in
				Spain can be one of life’s most rewarding journeys.
			</p>
		</div>
		<img src={authorPic} alt="Adrian Setka">
	</div>
</section>

<style>
    .author-section {
        padding: 80px 0;
        margin-left: 12vw;
        margin-right: 20vw;
        max-width: 1150px;
    }

    .author-container {
        display: flex;
        justify-content: space-between;
    }

    .author-container img {
        width: 40%;
        border: 6px solid black;
        box-shadow: 0 4px 24px rgba(0, 0, 0, 0.5);
    }

    .author-text {
        width: 55%;
    }

</style>