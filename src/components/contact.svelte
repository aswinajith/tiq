<script>
	import { page } from '$app/stores';
	function scrollToTop() {
		window.scroll({ top: 0, behavior: 'smooth' });
	}
	let tabs = $state([
		{ name: 'About Us', link: '/about' },
		{ name: 'Contact', link: '/contact' }
	]);
</script>

<div class="h-screen w-full relative flex flex-col">
	<div
		class="h-[40%] flex flex-col relative bg-gradient-to-tr from-[#622B19] from-0% via-[#532516] via-45%
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
	</div>
	<div class="bg-[#F8F3E2] h-[60%]"></div>
	<div
		class="flex flex-col absolute top-1/3 left-1/2 bg-[#EDCA90] -translate-x-1/2 -translate-y-1/2"
	>
		<h1 class="font-[merriweather] text-[#532516] text-center text-6xl mt-20 mb-10 mx-50">
			Contact Us
		</h1>
		<p class="text-base text-[#532516] mx-20 font-light leading-loose text-center">
			Call/text us or leave us an E-mail. If you have any comments, questions or concerns, please
			let us know. Our team will respond in 24hrs:-
		</p>
	</div>
</div>
