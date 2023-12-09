<template>
   <NavbarComponent />
   <HeroSection />
   <AwardsSection />
   <ParticipateSection />
   <AwardsListSection />
   <VideoSection />
   <ProductsSection />
   <BuySection />
   <FooterComponent />
</template>

<script>
import NavbarComponent from './components/NavbarComponent.vue'
import HeroSection from './components/HeroSection.vue'
import AwardsSection from './components/AwardsSection.vue';
import ParticipateSection from './components/ParticipateSection.vue'
import AwardsListSection from './components/AwardsListSection.vue';
import VideoSection from './components/VideoSection.vue';
import ProductsSection from './components/ProductsSection.vue'
import BuySection from './components/BuySection.vue'
import FooterComponent from './components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    NavbarComponent,
    HeroSection,
    AwardsSection,
    ParticipateSection,
    AwardsListSection,
    VideoSection,
    ProductsSection,
    BuySection,
    FooterComponent
  }
}
</script>

<style>
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
	vertical-align: baseline;
  font-family: Brandon;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}

@font-face {
    font-family: 'Latino';
    src: url('~@/assets/fonts/Latinotype-TrendSansFive.otf');
}

@font-face {
    font-family: 'Brandon';
    src: url('~@/assets/fonts/BrandonGrotesqueBlack.otf');
}


#app {
  text-align: center;
  background-color: #074A75;
}
</style>
