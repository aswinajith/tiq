<script>
	import { page } from '$app/stores';

	function scrollToTop() {
		window.scrollTo({ top: 0, behavior: 'smooth' });
	}

	let tabs = $state([
		{ name: 'About Us', link: '/about' },
		{ name: 'Contact', link: '#contact' }
	]);
</script>

<div
	class="flex flex-col relative bg-gradient-to-tr from-[#622B19] from-0% via-[#532516] via-45%
to-[#7B3C27] to-100%"
>
	<div class="flex overflow-hidden lg:flex-row md:flex-wrap sm:flex-wrap">
		<div class="flex flex-col flex-1">
			<header class="top-0 flex flex-row mt-2 font Nunito-Sans z-10 lg:pl-27 md:pl-10 sm:pl-0">
				<a href="/">
					<img class="w-20 h-21 -translate-y-3.5" src="../src/media/favicon.svg" alt="tiq" />
				</a>
				<div class="py-3.5 ml-auto text-xl">
					{#each tabs as tab}
						<a
							class="text-[#F8F3E2] px-7 font-light {$page.url.pathname === tab.link
								? 'underline underline-offset-10 font-extrabold'
								: ''}"
							href={tab.link}>{tab.name}</a
						>
					{/each}

					<a
						href="#Register"
						target="_blank"
						class="font-light blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-[#EDCA90] ml-7 mr-20"
					>
						Register
					</a>
				</div>
			</header>
		</div>
	</div>
	<div class="flex mx-35 my-25 mb-45 lg:flex-row">
		<div class="flex flex-col">
			<h1 class="text-6xl font-[merriweather] text-[#EDCA90] text-left">About Tiq</h1>
			<p class="mt-10 text-base text-[#EDCA90] leading-loose font-light mr-10 pr-30">
				The Illuminati Quiz (TIQ), the annual inter collegiate quiz competition organised by Govt.
				Model Engineering College is one of the largest student organised Quiz in South India. Held
				in memory of the late Sandeep Menon. Like the last edition, Illuminati Quiz will also be
				open to all categories testing the experience and mettle of working professionals against
				the young blood of quizzing.
			</p>
			<p class="mt-5 text-base text-[#EDCA90] leading-loose font-light mr-10 pr-30">
				The new normal paved way for quizeers accross the country to be part of this prestigious
				event. It also garners a large number of participants from elite colleges like IIMs and
				IITs, and numerous schools across South India and is well known not just for its attractive
				prize money but also for providing a convivial quizzing experience.
			</p>
		</div>
		<img class="h-100 relative ml-auto" src="/src/media/tiqyellow.png" alt="tiqlogo" />
	</div>
</div>
<div class="flex flex-row bg-[#EDCA90]">
	<img class="my-35 ml-30" src="/src/media/sandeep_menon.png" alt="Sandeep Menon" />
	<div class="ml-20 mt-40 flex flex-col">
		<h1 class=" font-normal text-6xl font-[merriweather] text-[#532516]">Sandeep Menon</h1>
		<h2 class="my-7 font-light text-4xl italic font-[merriweather] text-[#532516]">
			(1984) - (2008)
		</h2>
		<p class="text-base text-[#532516] mr-70 leading-8">
			Sandeep Menon (batch of 2006 - Model Engineering College) is the founder and guiding spirit of
			the 'The Illuminati'. An exceptional quizzer, he is affectionately known in local quizzing
			circles as 'The Illuminatus'. He was diagnosed with cancer in 2005. Despite deteriorating
			health, Sandeep pursued his academics with utmost commitment, led the placement cell to bring
			record number of jobs on campus and instilled the spirit of quizzing in MEC. Yet, his dream
			lives on through The lluminati and its marquee event, The Illuminati Quiz.
		</p>
	</div>
</div>
<div class="flex flex-col bg-[#F8F3E2]">
	<div class="flex flex-row items-center mt-30 ml-35">
		<img src="/src/media/college.png" alt="college" />
		<h1 class="ml-20 text-6xl text-[#532516] font-light font-[merriweather]">
			Govt. Model <br />Engineering College
		</h1>
	</div>
	<div class="flex flex-row mx-40 gap-10 mb-30 font-light font-[#532516] leading-loose">
		<p>
			Govt. Model Engineering College, Kochi, a premier institute of engineering education in Kerala
			is not just another engineering college producing hordes of engineering graduates every year.
			Nurturing a very diverse community of budding innovators and entrepreneurs, MEC has emblazoned
			its name as one of the most sought-after destinations for students and recruiters alike. This
			attests to MEC being ranked the 27th best engineering institute in the country.<br /><br
			/>Illuminati, the quizzing fraternity of Govt. Model Engineering College, Kochi is among the
			most active students' societies of the college having conducted atleast over a hundred intra
			and inter collegiate quizzes.
		</p>
		<p>
			Founded by the late Sandeep Menon to foster the spirit of quizzing in the student community,
			Illuminati has grown into a recognisable name all across South India. The Illuminati organizes
			the weekly Thank God Ifs Anyday (TGIX) intra college student quiz which spans a wide range of
			subjects while bringing together avid quizzers from among the students to test their mettle
			against each other in a battle of wits.
		</p>
	</div>
</div>
<button on:click={scrollToTop} class="fixed bottom-10 right-10 bg-[#3B2F2F] rounded-full p-3">
	<svg
		xmlns="http://www.w3.org/2000/svg"
		fill="none"
		viewBox="0 0 24 24"
		stroke-width="1.5"
		stroke="currentColor"
		class="size-6 fill-current text-white"
	>
		<path
			stroke-linecap="round"
			stroke-linejoin="round"
			d="M8.25 6.75 12 3m0 0 3.75 3.75M12 3v18"
		/>
	</svg>
</button>
