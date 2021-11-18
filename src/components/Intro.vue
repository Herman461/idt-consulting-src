<template>
	<section class="page__intro intro">
		<div class="intro__container _container">
			<div class="intro__body">
				<div class="intro__content">
					<h1 class="intro__title">Web technologies <span>for business</span></h1>
					<div class="intro__text">Lorem ipsum dolor sit amet, consectetur adipiscing elit,<br>sed do eiusmod tempor incididunt ut labore et</div>
					<form class="intro__form contact-form">
						<div class="contact-form__body">
							<div class="contact-form__row">
								<div class="contact-form__column">
									<div class="contact-form__label">Name</div>
									<div class="contact-form__input">
										<input autocomplete="off" type="text" placeholder="Your name" class="input">
									</div>
								</div>
								<div class="contact-form__column">
									<div class="contact-form__label">Phone number</div>
									<div class="contact-form__input">
										<input autocomplete="off" type="tel" placeholder="Your phone number" class="input">
									</div>
								</div>
							</div>
							<button class="contact-form__btn btn">contact us</button>
						</div>
					</form>
				</div>
				<div class="intro__image">
					<img src="img/test.png" alt="">
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: "intro-section"
}
</script>

<style lang="scss">
.intro {
	min-height: 100vh;
	position: relative;
	&__container {
		min-height: 100vh;
		display: flex;
		align-items: center;
		position: relative;
		padding: 130px 15px 50px 15px;
		@media (max-width: $md2+px) {
			padding: 110px 15px 50px 15px;
		}
		&::before {
			@media (min-width: 1060px) {
				content: '';
				position: absolute;
				top: 0;
				left: 708px;
				width: 100%;
				height: 100%;
				background-color: $greenColor;
				border-bottom-left-radius: 20px;
			}
			@media (min-width: $md1+px) {
				left: 55.2%;
				border-bottom-left-radius: 50px;
			}
		}
	}
	&__image {
		@media (min-width: $md1+px) {
			flex: 0 0 444px;
		}
		@media (min-width: 1060px) {
			position: relative;
			z-index: 3;
			flex: 0 0 400px;
			img {
				max-width: 100%;
			}
		}
		@media (max-width: 1060px) {
			display: none;
		}
	}
	&__body {
		@media (min-width: 1060px) {
			display: flex;
			align-items: center;
		}
		@media (max-width: 1060px) {
			width: 100%;
		}
	}
	&__content {
		@media (min-width: 1060px) {
			flex: 0 0 600px;
			padding: 0px 33px 0px 0px;
		}
		@media (min-width: $md1+px) {
			flex: 0 0 658px;
		}
	}
	&__title {
		@include adaptiv-value("font-size", 41, 29, 1);
		font-size: 41px;
		text-transform: uppercase;
		font-weight: 700;
		&:not(:last-child) {
			margin: 0px 0px 13 / 41 * 1em 0px;
		}
		
		span {
			display: block;
			color: $greenColor;
			@include adaptiv-value("font-size", 60, 35, 1);
		}
	}
	
	&__text {
		line-height: 18px;
		font-weight: 500;
		&:not(:last-child) {
			@include adaptiv-value("margin-bottom", 50, 30, 1);
		}
		@media (max-width: 1060px) {
			br {
				display: none;
			}
		}
	}
}
</style>