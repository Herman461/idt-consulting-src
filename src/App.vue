<template>
	<!-- <div class="wrapper">
		<HeaderComponent />
		<main class="page">
			<IntroSection />
			<AboutSection />
			<TechnologiesSection />
			<ContactsSection />
		</main>
		<FooterComponent />
	</div> -->
</template>

<script>
import HeaderComponent from '@/components/Header';
import IntroSection from '@/components/Intro';
import AboutSection from '@/components/About';
import TechnologiesSection from '@/components/Technologies';
import ContactsSection from '@/components/Contacts';
import FooterComponent from '@/components/Footer';

export default {
	name: 'app',
	components: {
		HeaderComponent,
		IntroSection,
		AboutSection,
		TechnologiesSection,
		ContactsSection,
		FooterComponent
	}
}
</script>

<style lang="scss">
	
</style>
