<template>
   <section class="page__contacts contacts">
      <div class="contacts__container _container">
         <h2 class="contacts__title _title">Contacts</h2>
         <div class="contacts__items">
            <a href="tel:+4222222222" class="contacts__item fas fa-phone">+422 2222222</a>
            <a href="" class="contacts__item fas fa-map-marker">Praha 8, Troja, Pomořanská 475/8</a>
            <a href="mailto:josef.novotny@ltd.com" class="contacts__item fas fa-envelope"
               >josef.novotny@ltd.com</a
            >
         </div>
         <div class="contacts__bottom">
            <div class="contacts__social social-contacts">
               <a href="" class="social-contacts__item">
                  <img src="img/icons/social/facebook.png" alt="">
               </a>
               <a href="" class="social-contacts__item">
                  <img src="img/icons/social/youtube.png" alt="">
               </a>
               <a href="" class="social-contacts__item">
                  <img src="img/icons/social/instagram.png" alt="">
               </a>
            </div>
            <form class="contacts__form contact-form">
               <div class="contact-form__body contact-form__body_bottom">
                  <div class="contact-form__row">
                     <div class="contact-form__column">
                        <div class="contact-form__label">Name</div>
                        <div class="contact-form__input">
                           <input
                              autocomplete="off"
                              type="text"
                              placeholder="Your name"
                              class="input"
                           >
                        </div>
                     </div>
                     <div class="contact-form__column">
                        <div class="contact-form__label">Phone number</div>
                        <div class="contact-form__input">
                           <input
                              autocomplete="off"
                              type="tel"
                              placeholder="Your phone number"
                              class="input"
                           >
                        </div>
                     </div>
                  </div>
                  <button class="contact-form__btn contact-form__btn_center btn">contact us</button>
               </div>
            </form>
         </div>
      </div>
   </section>
</template>

<script>
export default {
	name: "contacts-section"
}
</script>

<style lang="scss">

.contacts {

	&__container {
	}

	&__title {
		&:not(:last-child) {
			@include adaptiv-value("margin-bottom", 43, 24, 1);
		}
	}

	&__items {
		
		&:not(:last-child) {
			@include adaptiv-value("margin-bottom", 84, 30, 1);
		}
		display: flex;
		@media (max-width: 860px) {
			flex-direction: column;
		}
	}

	&__item {
		
		font-size: 18px;
		font-weight: 500;
		display: inline-flex;
		line-height: 22 / 18  * 100%;
		align-items: center;
		color: inherit;
		@media (min-width: 860px) {
			flex: 0 1 33.333%;
		}

		&:not(:last-child) {
			margin: 0px 20px 0px 0px;
		}
		&::before {
			margin: 0px 12px 0px 0px;
			flex: 0 0 52px;
			min-height: 52px;
			@media (max-width: $md2+px) {
				width: 43px;
				flex: 0 0 43px;
				min-height: 43px;
			}
			font-size: 24px;
			color: #fff;
			border-radius: 50%;
			background-color: $greenColor;
			display: inline-flex;
			justify-content: center;
			align-items: center;
		}
		@media (max-width: 860px) {
			&:not(:last-child) {
				margin: 0px 0px 25px 0px;
			}
		}
		@media (max-width: $md1+px) {
			font-size: 16px;
			&::before {
				font-size: 20px;
			}
		}
	}

	&__bottom {
		@media (min-width: 860px) {
			display: flex;
			align-items: flex-start;
		}
	}

	&__social {
		@media (max-width: 860px) {
			margin: 0px 0px 30px 0px;
		}
	}

	&__form {
		@media (min-width: 860px) {
			flex: 1 1 auto;
			padding: 0px 0px 0px 240 / $maxWidthContainer * 100%;
		}

	}
}
.social-contacts {
	display: flex;
	&__item {
		&:not(:last-child) {
			margin: 0px 30px 0px 0px;
		}
	}
}

</style>