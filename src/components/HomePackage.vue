<script>
export default {
    data() {
        return {
            cards: [
                { title: 'Great Ocean Road , Australia', days: '5 Days Tour', price: '$2700/couple', location: 'Ocean Road , Australia', place: 'Near Mountain', image: '/assets/Package_Slider-1-a3a12458.webp', bookLink: '#' },
                { title: 'Great Ocean Road , Australia', days: '11 Days Tour', price: '$3400/person', location: 'Ocean Road , Australia', place: 'Near Mountain', image: '/assets/Package_Slider-2-742083f5.webp', bookLink: '#' },
                { title: 'Great Ocean Road , Australia', days: '8 Days Tour', price: '$300/person', location: 'Ocean Road , Australia', place: 'Near Mountain', image: '/assets/Package_Slider-3-162cf4c1.webp', bookLink: '#' },
                { title: 'Great Ocean Road , Australia', days: '8 Days Tour', price: '$300/person', location: 'Ocean Road , Australia', place: 'Near Mountain', image: '/assets/Package_Slider-4-fc72198b.webp', bookLink: '#' },
                { title: 'Great Ocean Road , Australia', days: '8 Days Tour', price: '$300/person', location: 'Ocean Road , Australia', place: 'Near Mountain', image: '/assets/Package_Slider-5-85f7ef18.webp', bookLink: '#' },
                { title: 'Great Ocean Road , Australia', days: '8 Days Tour', price: '$300/person', location: 'Ocean Road , Australia', place: 'Near Mountain', image: '/assets/Package_Slider-6-09ba78b8.jpeg', bookLink: '#' }
            ]
        };
    },
    mounted() {
        this.setupSlider();
    },
    methods: {
        setupSlider() {
            const cardsContainer = this.$el.querySelector('.card-content');
            const cardWidth = window.innerWidth / 2 > 600 ? window.innerWidth / 2 : window.innerWidth - 100;
            let currentIndex = 0;

            this.handleScrollNext = () => {
                currentIndex = (currentIndex + 1) % cardsContainer.children.length;
                this.scrollSlider();
            };

            this.handleScrollPrev = () => {
                currentIndex = (currentIndex - 1 + cardsContainer.children.length) % cardsContainer.children.length;
                this.scrollSlider();
            };

            this.scrollSlider = () => {
                const scrollAmount = currentIndex * cardWidth;
                cardsContainer.scrollLeft = scrollAmount;

                if (currentIndex === cardsContainer.children.length - 1) {
                currentIndex = 0;
                cardsContainer.scrollLeft = 0;
                }
            };
        },
    },
};
</script>

<template>
    
    <section class="Package fh5co-cta">
        <div class="overlay"></div>

        <div class="container Package-container" data-zanim-timeline="{}">
            <h2 class="Title" data-zanim-xs='{"delay":0.1}'>Package Tour</h2>
            <p class="description" data-zanim-xs='{"delay":0.2}'>Get ready for starting tour</p>

            <button id="prev" class="btn" @click="handleScrollPrev">
                    <i class="las la-angle-left"></i>
                </button>

                <button  id="next" class="btn" @click="handleScrollNext">
                    <i class="las la-angle-right"></i>
                </button>

            <div class="slider">

                <div class="card-content" ref="cardContent">
                    <div class="card" v-for="(card, index) in cards" :key="index">
                        <div class="Package-card-img">
                            <img :src="card.image" alt="">
                        </div>
                        <div class="card-text">
                            <span class="days">{{ card.days }}</span>
                            <span class="price">{{ card.price }}</span>
                            <h2>{{ card.title }}</h2>
                            <p class="location"><span class="fas fa-map"></span>{{ card.location }}</p>
                            <p class="place"><span class="fas fa-mountain"></span>{{ card.place }}</p>
                            <a class="btn btn-outline-primary rounded-pill btn-sm border-2 d-block d-lg-inline-block ms-auto my-3 my-lg-0" :href="card.bookLink" target="_blank">Book Now</a>
                        </div>
                    </div>
                </div>
                
            </div>

        </div>

    </section>

</template>

<style scoped>
.Package{
    padding-bottom: 40px;
}
.First_svg{
    margin-top: -120px;
}
.fh5co-cta{
	background-image: url(../../assets/img/Travel/Package/package-bg.jpg);
	height: auto;
    z-index: 1;
}
.fh5co-cta .overlay {
    background-color: rgba(0,0,0,.6);
    opacity: .83;
    transition: background .3s,border-radius .3s,opacity .3s;
    left: 0;
    right: 0;
    bottom: 0;
    top: 0;
    position: absolute;
    z-index: -1;
    height: auto;
}
.Package-container{
    margin-top: -130px;
}
.Title{
    color: #fd9604 !important;
    font-family: 'Fira Sans', sans-serif;
    letter-spacing: 1px;
    text-align: start;
    margin-top: 100px;
}
.description{
    font-size: 20px;
    font-family: 'Fira Sans', sans-serif;
    color: #cacaca;
}
.CardSlider{
    padding-top: 4.5rem;
    overflow: hidden !important;
}
.card {
  width: 320px;
  min-width: 320px;
  height:auto;
  background:#fff;
  position:relative;
  z-index:10;
  margin:25px;
  min-height:356px;
  cursor:pointer;
  transition: all .25s ease;
  border: none;
  box-shadow: 0px 0px 0px 0px rgba(0,0,0, .08);
  border-radius: 0%;
}

.card:hover {
  transform:translate(0, -10px);
}

.card h4 {
  position:absolute;
  left: 0;
  top: 0;
  padding: 15px;
  color: #fd9604;
}

.card i {
  position:absolute;
  right: 0;
  top: 0;
  padding: 15px;
  font-size:1.4rem;
  line-height:3.2rem;
}
.card-text{
    position: relative;
    border: 1px solid rgba(0, 0, 0, 0.08);
    border-top: none;
}
.card-text span{
    font-size: 12px; 
    color: #999999;
}
.location{
    font-size: 14px;
    line-height: 1.8;
    font-weight: 400;
    color: #999999;
}
.location .fa-map{
    font-size: 13px;
    color: #999999;
    margin: 0px 5px;
}
.place{
    font-size: 16px;
    line-height: 1.8;
    font-weight: 400;
    color: #999999;
}
.place .fa-mountain{
    font-size: 13px;
    color: #f9ab30;
    margin: 0px 5px;
}
.card .card-text .price {
    position: absolute;
    top: -23px;
    left: 50%;
    -ms-transform: translateX(-50%);
    transform: translateX(-50%);
    display: inline-block;
    background: #f9ab30;
    color: #fff;
    margin: 0 auto;
    padding: 8px;
    font-size: 16px;
    -webkit-border-radius: 40px;
    -moz-border-radius: 40px;
    -ms-border-radius: 40px;
    border-radius: 40px;
    -moz-transition: all 0.3s ease;
    -o-transition: all 0.3s ease;
    -webkit-transition: all 0.3s ease;
    -ms-transition: all 0.3s ease;
    transition: all 0.3s ease;
}
.card:hover .card-text .price {
    padding-left: 15px;
    padding-right: 15px;
    background: #33313b;
}
/* .card:hover img {
    transform: scale(1.1);
} */
.card .card-text {
    padding: 15px;
    border-bottom-left-radius: 30px;
    border-bottom-right-radius: 30px;
}

.card-text h2{
    color: #0b3ba7;
    font-size: 20px;
    font-family: 'Fira Sans', sans-serif;
    letter-spacing: 1px;
    margin-top: 10px;
}
p {
    font-size: 15px;
    font-weight: 600;
    margin-top: 10px;
    color: #676060;
}
.btn-outline-primary{
    width: 110px;
    padding: 10px;
    height: 36px !important;
    background: transparent !important;
    color: #000 !important;
    border: 1px solid #0b3ba7 !important;
    margin-top: 15px !important;
}
.btn-outline-primary:hover{
    background: #0b3ba7 !important;
    color: #fff !important;
}
.card img {
    width: 100%;
    height: 200px;
    transition: transform 0.3s ease;
}
.card-content {
  display:flex;
  align-items:center;
  justify-content:flex-start;
  width:100%;
  overflow:auto;
  padding-top: 100px;
  padding-right: 50px;
  scroll-behavior:smooth;
}
.card-content::-webkit-scrollbar {
   height:0px;
}
.card-content:after {
  content:'';
  display:block;
  min-width:20px;
  height:100px;
  position:relative;
}
.btn{
  min-width:50px;
  margin:auto 10px;
  height:60px;
  padding: 6px;
  font-family: 'Open Sans', sans-serif;
  font-weight: 600;
  letter-spacing: 0.5px;
  border-radius:20px;
  background:#0b3ba7;
  color: #fff;
  border:0px;
  outline:none;
  cursor:pointer;
  z-index:9999;
  box-shadow: 0px 0px 0px 0px rgba(0,0,0,.08);
  transition: all .25s ease;
}
#prev {
    width: 50px !important;
    height: 50px!important;
    border-radius: 50%;
    margin-top: -175px;
    margin-left: 85%;
    padding: 0;
}
#next {
    width: 50px !important;
    height: 50px!important;
    border-radius: 50%;
    margin-top: -222px;
    margin-left: 91%;
    padding: 0;
}
.btn:hover{
    background:transparent;
    border: 1px solid #f9ab30;
    color: #f9ab30;
    box-shadow: 0px 17px 35px 0px rgba(0,0,0,.07);
}

.btn i {
  font-size:1.2rem;
}

.slider {
    display: block;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: auto;
    padding-bottom: 15px;
    overflow: hidden;
    margin-top: -100px;
}
.line{
    position: absolute;
    left: 575px;
    width: 90px;
    height: 5px;
    background-color: #fd9604;
    border-radius: 10px;
}
@media screen and (max-width: 768px) {
    .Package{
        overflow: hidden !important;
    }
    .Title{
        font-size: 25px;
    }
    .description{
        font-size: 12px;
    }
    #prev{
        margin-left: 60%;
        margin-top: 10px;
    }
    #next{
        margin-left: 80%;
        margin-top: -70px;
    }
    .First_svg{
        margin-top: -65px;
        height: 200px;
    }

    .Package-container {
        margin-top: -85px;
    }
    .card{
        width: 100% !important;
        min-width: 255px;
        margin: 0px 20px;
    }
    .card-text h2{
        font-size: 18px;
    }
    .Package-card-img{
        width: 100%;
    }
    .btn{
        margin-top: 10px;
    }
}
</style>