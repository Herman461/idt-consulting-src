<template>
   <section class="page__about about">
      <div class="about__container _container">
         <div class="about__block">
            <h2 class="about__title _title">About us</h2>
            <div class="about__image _ibg">
               <img src="img/about.jpg" alt="">
            </div>
         </div>
         <div class="about__content">
            <div class="about__items">
               <div class="about__item item-about">
                  <div class="item-about__icon">
                     <img src="img/icons/about/01.png" alt="">
                  </div>
                  <div class="item-about__text">
                     Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                     incididunt
                  </div>
               </div>
               <div class="about__item item-about">
                  <div class="item-about__icon">
                     <img src="img/icons/about/02.png" alt="">
                  </div>
                  <div class="item-about__text">
                     Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                     incididunt
                  </div>
               </div>
               <div class="about__item item-about">
                  <div class="item-about__icon">
                     <img src="img/icons/about/03.png" alt="">
                  </div>
                  <div class="item-about__text">
                     Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                     incididunt
                  </div>
               </div>
               <div class="about__item item-about">
                  <div class="item-about__icon">
                     <img src="img/icons/about/04.png" alt="">
                  </div>
                  <div class="item-about__text">
                     Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
                     incididunt
                  </div>
               </div>
            </div>
         </div>
      </div>
   </section>
</template>

<script>
export default {
	name: "about-section"
}
</script>

<style lang="scss">
.about {
	&__container {
		@media (min-width: 1080px) {
			display: flex;
			align-items: center;
		}
	}
	&__block {
		position: relative;
		@media (min-width: 1080px) {
			flex: 0 0 800 / $maxWidthContainer * 100%;
		}
		@media (max-width: 1080px) {
			margin: 0px -15px 30px -15px;
		}
	}
	
	&__title {
		text-align: left;
		position: absolute;
		z-index: 0;
		left: 110px;
		top: 26px;
		z-index: 2;
		@media (max-width: $md1+px) {
			left: 15px;
		}
	}
	
	&__image {
		width: 100%;
		padding: 0px 0px 71.1% 0px;
		@media (max-width: 1080px) {
			padding: 0px 0px 40% 0px;
		}
		@media (max-width: $md3+px) {
			padding: 0px 0px 70% 0px;
		}
	}
	&__content {
		@media (min-width: 1080px) {
			flex: 1 1 auto;
			padding: 0px 0px 0px 71 / $maxWidthContainer * 100%;
		}
		
	}
	&__items {
		
		position: relative;
		&:before {
			content: '';
			width: 5px;
			height: calc(100% - 6px);
			position: absolute;
			top: 6px;
			left: 3px;
			// background: url('../img/dotts.png') 0 0 repeat;
		}
	}
	
	&__item {
		&:not(:last-child) {
			margin: 0px 0px 70px 0px;
		}
		&:first-child,
		&:last-child {
			position: relative;
			z-index: 2;
			background-color: #fff;
		}
	}
}

.item-about {
	display: flex;
	position: relative;
	align-items: center;
	&:before {
		content: '';
		display: block;
		border-radius: 50%;
		flex: 0 0 12px;
		align-self: center;
		margin: 0px 38px 0px 0px;
		height: 12px;
		background-color: #323232;
		position: relative;
		z-index: 2;
		@media (max-width: $md3+px) {
			margin: 0px 25px 0px 0px;
		}
	}
	&:after {
		content: '';
		height: 54px;
		width: 12px;
		display: block;
		position: absolute;
		background-color: #fff;
		top: 50%;
		left: 0;
		transform: translate(0, -50%);
	}
	&__icon {
		flex: 0 0 66px;
		img {
			max-width: 100%;
		}
	}
	
	&__text {
		flex: 1 1 auto;
		line-height: 18px;
		padding: 0px 0px 0px 20px;
	}
}

</style>