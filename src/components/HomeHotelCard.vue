<script>
// Assuming you are using Vue.js
export default {
    data() {
        return {
            cards: [
                { title: 'Basket Ball', rating: 4.5, image: 'https://images.pexels.com/photos/258154/pexels-photo-258154.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1', description: 'I show you how to make a card group easily and very functional with the use of flexbox and its magic and JavaScript.', bookLink: '#' },
                { title: 'Volley Ball', rating: 4.4, image: 'https://images.pexels.com/photos/1375383/pexels-photo-1375383.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1', description: 'I show you how to make a card group easily and very functional with the use of flexbox and its magic and JavaScript.', bookLink: '#' },
                { title: 'Disco Ball', rating: 4.7, image: 'https://images.pexels.com/photos/60217/pexels-photo-60217.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1', description: 'I show you how to make a card group easily and very functional with the use of flexbox and its magic and JavaScript.', bookLink: '#' },
                { title: 'Blue Ball', rating: 4.2, image: 'https://images.pexels.com/photos/261101/pexels-photo-261101.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1', description: 'I show you how to make a card group easily and very functional with the use of flexbox and its magic and JavaScript.', bookLink: '#' },
                { title: 'Green Ball', rating: 4.1, image: 'https://images.pexels.com/photos/1287460/pexels-photo-1287460.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1', description: 'I show you how to make a card group easily and very functional with the use of flexbox and its magic and JavaScript.', bookLink: '#' },
                { title: 'Red Ball', rating: 4.3, image: 'https://images.pexels.com/photos/13581464/pexels-photo-13581464.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1', description: 'I show you how to make a card group easily and very functional with the use of flexbox and its magic and JavaScript.', bookLink: '#' },
                // Add more cards as needed
            ],
            currentIndex: 0
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
                this.scrollSlider(cardsContainer, cardWidth, currentIndex);
            };

            this.handleScrollPrev = () => {
                currentIndex = (currentIndex - 1 + cardsContainer.children.length) % cardsContainer.children.length;
                this.scrollSlider(cardsContainer, cardWidth, currentIndex);
            };

            this.scrollSlider = (container, width, index) => {
                const scrollAmount = index * width;
                container.scrollLeft = scrollAmount;

                if (index === container.children.length - 1) {
                    index = 0;
                    container.scrollLeft = 0;
                }
            };

            // Add event listeners to navigation buttons
            const nextButton = this.$el.querySelector('.next-button');
            const prevButton = this.$el.querySelector('.prev-button');

            nextButton.addEventListener('click', this.handleScrollNext);
            prevButton.addEventListener('click', this.handleScrollPrev);
        },
    },

};

</script>

<template>

    <section class="CardSlider">
        <h2 class="Title">Hotel <span>Deals</span></h2>

        <div class="line"></div>


        <!-- <div class="container">
            <div class="row"> -->

                <div class="slider">
                    <button id="prev" class="btn prev-button">
                        <i class="las la-angle-left"></i>
                    </button>
                    
                    <div class="card-content">
                        <!-- Card -->
                        <div class="card" v-for="(card, index) in cards" :key="index">
                            <h4>{{ card.rating }}</h4>
                            <i class="lar la-heart"></i>
                            <div class="card-img">
                                <img :src="card.image" :alt="card.title">
                            </div>
                            <div class="card-text">
                                <h2>{{ card.title }}</h2>
                                <p>{{ card.description }}</p>
                                <a class="btn btn-outline-primary rounded-pill btn-sm border-2 d-block d-lg-inline-block ms-auto my-3 my-lg-0" :href="card.bookLink" target="_blank">Book Now</a>
                            </div>
                        </div>
                        <!-- Card End -->
                        
                    </div>
                    <button id="next" class="btn next-button">
                        <i class="las la-angle-right"></i>
                    </button>
                </div>

            <!-- </div>
        </div> -->
    </section>

</template>

<style scoped>
.CardSlider{
    padding-top: 4.5rem;
    overflow: hidden !important;
}
.Title{
    color: #0b3ba7 !important;
    font-family: 'Fira Sans', sans-serif;
    letter-spacing: 1px;
    text-align: center;
}
.Title span{
    color: #fd9604;
}
.card {
  width: 300px;
  min-width: 300px;
  height:auto;
  background:#fff;
  border-radius:30px;
  position:relative;
  z-index:10;
  margin:25px;
  min-height:356px;
  cursor:pointer;
  transition: all .25s ease;
  border: none;
  box-shadow: 0px 0px 0px 0px rgba(0,0,0, .08);
}

.card:hover {
  transform:translate(0, -10px);
  box-shadow: 0px 17px 35px 0px rgba(0,0,0,.07);
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

.card .card-text {
    box-shadow: 0px 17px 35px 0px rgba(0,0,0,.07);
    padding: 20px;
    border-bottom-left-radius: 30px;
    border-bottom-right-radius: 30px;
}

.card-text h2{
    color: #0b3ba7;
    font-size: 25px;
    font-family: 'Fira Sans', sans-serif;
    letter-spacing: 1px;
}
p {
  font-size: .8rem;
  opacity: .6;
  margin-top: 10px;
}
.btn-outline-primary{
    width: 110px;
    padding: 10px;
    height: 36px !important;
    background: transparent !important;
    color: #000 !important;
    border: 1px solid #0b3ba7 !important;
}
.btn-outline-primary:hover{
    background: #0b3ba7 !important;
    color: #fff !important;
}
.card img {
    width: 100%;
    border-top-left-radius: 30px;
    border-top-right-radius: 30px;
    height: 200px;

}
.card-content {
  display:flex;
  align-items:center;
  justify-content:flex-start;
  width:100%;
  overflow:auto;
  padding-top: 100px;
  padding-left:60px;
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
  background:#fd9604;
  color: #fff;
  border:0px;
  outline:none;
  cursor:pointer;
  z-index:9999;
  box-shadow: 0px 0px 0px 0px rgba(0,0,0,.08);
  transition: all .25s ease;
}

.btn:hover{
  box-shadow: 0px 17px 35px 0px rgba(0,0,0,.07);
}

.btn i {
  font-size:1.2rem;
}

.slider {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: auto;
    padding-bottom: 15px;
    overflow: hidden;
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
    .card-content {
        width: 100%;
        padding: 0;
    }
    .slider{
        display: block;
        margin-top: -50px;
    }
    .card{
        margin-left:10px;
    }
    #prev {
        width: 30px !important;
        height: 30px!important;
        margin-top: 80px;
        margin-left: 62%;
        padding: 0;
    }
    #next {
        width: 30px !important;
        height: 30px!important;
        margin-top: -963px;
        margin-left: 80%;
        padding: 0;
    }
    .slider:before{
        display: none;
    }
    .slider:after{
        display: none;
    }
}
</style>