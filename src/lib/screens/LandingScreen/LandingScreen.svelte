<script lang="ts">
	import HeroImage from '$assets/images/ganesh-hero-compressed.jpg';
	import Shiva from '$assets/images/shiva.jpg';
	import ServicesCarousel from '$components/ServicesCarousel.svelte';
</script>

<section
	id="main-section"
	class="mt-20 sm:mt-[120px] rounded-xl flex flex-col min-h-[70vh] relative justify-center overflow-hidden"
>
	<div class="absolute inset-0 z-[1] bg-secondary bg-opacity-85"></div>
	<div
		class="relative space-y-4 sm:px-10 py-10 px-4 sm:w-1/2 text-tertiary z-[2] flex-grow flex flex-col justify-center"
	>
		<h2 class="text-2xl">Welcome to Astro Shiva</h2>
		<h1 class="text-4xl font-bold">Discover Your Destiny Today!</h1>
		<p>
			Unlock the secrets of the universe with our expert astrology services, personalized readings
			and guidance for a bright future.
		</p>
		<span class="text-xl capitalize">Explore our services below</span>
	</div>

	<img src={HeroImage} alt="Astro Shiva" class="absolute object-cover object-top w-full h-full" />
</section>

<section id="services-section" class="mt-20">
	<h2 class="text-3xl font-semibold text-tertiary rounded-xl">Our Services</h2>

	<div class="p-2">
		<ServicesCarousel />
	</div>
</section>

<section
	id="about-us-section"
	class="relative px-4 py-10 mt-20 overflow-hidden rounded-xl bg-amber-700"
>
	<h2 class="text-3xl font-semibold text-tertiary rounded-xl">About Us</h2>

	<div class="relative p-2 z-[2]">
		<p class="text-sm sm:w-[60%] line-clamp-6">
			Astro shiva is the leading astrology media brand.
			<br /><br />With personalized readings and a vast library of astrology information, our site
			has the most to offer for beginners, learners, and professionals alike. Astrology.com offers
			cutting edge content, fresh daily horoscopes, detailed astrology reports, and a
			hyper-personalized subscription service, Astrology+.
			<br /> <br />Coming from a team who loves astrology as much as you do, Astrology+ is the first
			service to offer real-time transit notifications, birth chart analysis, live Q&As, and
			personalized moon reports—all in one place!<br /> <br /> Recognized by Digiday for Best Overall
			Design, with authenticity at the core of our ethos, we are proud to represent professional astrologers
			of all practices and backgrounds—making our site perfectly attuned for both the astro-curious and
			astro-serious
		</p>

		<h3 class="mt-4 mb-3 text-xl font-bold">What is Astrology?</h3>
		<p class="text-sm">
			The study of the positions and movements of the stars and planets and the way that some people
			believe they affect people and events. सौर-ग्रहों तथा तारों की स्थितियों एवं गतियों और उनका
			मानव जीवन और घटनाओं पर प्रभाव का अध्ययन; फलित ज्‍योतिष|
		</p>
	</div>
</section>
