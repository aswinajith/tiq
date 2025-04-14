<script>
	let tabs = $state([
		{ name: 'About Us', link: '#about' },
		{ name: 'Contact', link: '#contact' }
	]);
</script>

<div
	class="flex flex-col relative bg-gradient-to-tr from-[#622B19] from-0% via-[#532516] via-45%
to-[#7B3C27] to-100%"
>
	<div class="flex overflow-hidden lg:flex-row md:flex-wrap sm:flex-wrap">
		<div class="flex flex-col flex-1">
			<header
				class="sticky top-0 flex flex-row mt-2 font Nunito-Sans z-10 lg:pl-27 md:pl-10 sm:pl-0"
			>
				<img class="w-20 h-21 -translate-y-3.5" src="../src/media/favicon.svg" alt="tiq" />

				<div class="pr-0 py-3.5 px-10 text-xl">
					{#each tabs as tab}
						<a class="text-[#F8F3E2] px-7 font-light" href={tab.link}>{tab.name}</a>
					{/each}

					<a
						href="#Register"
						target="_blank"
						class="font-light blueShadow relative overflow-hidden px-5 py-2 group rounded-full bg-[#EDCA90] ml-7"
					>
						Register
					</a>
				</div>
			</header>
			<div>
				<h1
					class="relative text-[#F8F3E2] text-8xl text-left
                mt-20 ml-30 w-32 font-[merriweather] z-10"
				>
					THE ILLUMINATI QUIZ
				</h1>

				<h1
					class="relative text-[#E5BAA7]
                text-2xl mt-10 ml-30 italic"
				>
					An open quiz in memory of Sandeep Menon
				</h1>
			</div>
		</div>
		<img
			class="ml-auto h-120 lg:-translate-x-30 md:-translate-x-10"
			src="../src/media/Frame46.png"
			alt="speaker"
		/>
	</div>
	<div class="flex flex-row-reverse relative">
		<div class="flex flex-col relative px-10">
			<img class="w-30" src="../src/media/Frame4.png" alt="round speaker" />
			<p class="text-right mt-3 w-40 -translate-x-10 text-[#E5BAA7] italic">
				Hosted by Major Chandrakanth Nair
			</p>
		</div>
		<img class="px-15" src="../src/media/Frame45.png" alt="speaker" />
	</div>
</div>
