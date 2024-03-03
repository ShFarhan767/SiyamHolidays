<script setup>
const airlines = [
    {
        name: 'AIR MALTA',
        code: 'KM',
        className: 'fh5co-cta',
        logo: 'https://upload.wikimedia.org/wikipedia/en/6/6b/Logo_airmalta.svg',
        phoneNumbers: {
            AU: '1300 748 747',
            NZ: '0800 039 339',
            INT: '+61 2 9250 9444'
        },
        email: 'airmaltaserv@gmail.com',
        flightLink: '#'
    },
    {
        name: 'AIR SERBIA',
        code: 'JU',
        className: 'fh5co-cta-one',
        logo: 'https://upload.wikimedia.org/wikipedia/de/thumb/b/bf/Air_Serbia_Logo.svg/2560px-Air_Serbia_Logo.svg.png',
        phoneNumbers: {
            AU: '1300 748 747',
            NZ: '0800 039 339',
            INT: '+61 2 9250 9444'
        },
        email: 'airmaltaserv@gmail.com',
        flightLink: '#'
    },
    {
        name: 'ALITALIA',
        code: 'AZ',
        className: 'fh5co-cta-two',
        logo: 'https://upload.wikimedia.org/wikipedia/en/thumb/3/34/Alitalia_logo.svg/2560px-Alitalia_logo.svg.png',
        phoneNumbers: {
            AU: '1300 748 747',
            NZ: '0800 039 339',
            INT: '+61 2 9250 9444'
        },
        email: 'airmaltaserv@gmail.com',
        flightLink: '#'
    },
    {
        name: 'BRUSSELS',
        code: 'SN',
        className: 'fh5co-cta-three',
        logo: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/bb/Brussels_airlines_logo_2021.svg/2560px-Brussels_airlines_logo_2021.svg.png',
        phoneNumbers: {
            AU: '1300 748 747',
            NZ: '0800 039 339',
            INT: '+61 2 9250 9444'
        },
        email: 'airmaltaserv@gmail.com',
        flightLink: '#'
    }
];
</script>

<template>

    <section class="Flight">
        <div class="container ">
            <h3>Featured Flight</h3>
            <p><i class="fas fa-fighter-jet"></i></p>

            <div class="slider">

                <div class="card-content">
                    <!-- Card -->
                    <div class="card" v-for="(airline, index) in airlines" :key="index">
                        <a :href="airline.flightLink">
                            <div class="card-img">
                                <img :src="airline.logo" :alt="airline.name">
                            </div>
                            <div class="card-text">
                                <div :class="airline.className">
                                    <div class="overlay"></div>
                                    <div class="container">
                                        <div class="col-md-12 text-center animate-box">
                                            <h4>{{ airline.name }} ({{ airline.code }})</h4><br>
                                            <ul>
                                                <li v-for="(number, location) in airline.phoneNumbers" :key="location">
                                                    {{ location }}:<span>{{ number }}</span>
                                                </li>
                                            </ul>
                                            <h5>SEND US EMAIL </h5>
                                            <h6>{{ airline.email }}</h6>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </a>
                    </div>

                        
                </div>

            </div>

        </div>

    </section>

</template>

<style scoped>
.Flight{
    width: 100%;
    height: auto;
    background: url(https://www.designbolts.com/wp-content/uploads/2021/01/rainy-clouds-with-blue-sky-wallpaper-1.jpg) no-repeat;
    background-size: cover;
    padding-top: 0;
    padding-bottom: 15px;
    padding-left: 0px;
    margin-left: 0px;
    overflow: hidden !important;
}
.Flight h3{
    font-family: 'Fira Sans', sans-serif;
    text-align: center;
    color: #fff;
    font-size: 36px;
    letter-spacing: 1px;
    margin-top: 35px;
}
.Flight p{
    font-size: 18px;
    color: #fff;
    position: relative;
    display: inline-block;
    margin-left: 50%;
}
.fa-fighter-jet{
    transform: rotateZ(-46deg);
}
.Flight p::before,
.Flight p::after {
  content: '';
  position: absolute;
  top: 50%;
  width: 50px; 
  height: 1px; 
  background-color: #fff; 
}
.Flight p::before {
  left: -60px;
}
.Flight p::after {
  right: -60px; 
}
.slider {
    display: block;
    align-items: center;
    justify-content: center;
    width: 100%;
    height: auto;
    padding-bottom: 15px;
    overflow: hidden;
    margin-top: 35px !important;
}
.CardSlider{
    padding-top: 4.5rem;
    overflow: hidden !important;
}
.card {
    width: 250px;
    min-width: 250px;
    height: 410px;
    padding: 10px;
    border-radius: 30px;
    position: relative;
    z-index: 10;
    margin: 13px;
    min-height: 356px;
    cursor: pointer;
    float: left;
    transition: all .25s ease;
    border: none;
    box-shadow: 0px 0px 0px 0px rgba(0,0,0, .08);
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
.card-text h2{
    color: #0b3ba7;
    font-size: 20px;
    font-family: 'Fira Sans', sans-serif;
    letter-spacing: 1px;
    margin-top: 10px;
}
.card-text h4{
    font-family: 'Open Sans', sans-serif;
    color: #fff !important;
    padding: 20px;
    font-size: 22px;
    z-index: 1;
}
.card-text h5{
    font-family: 'Open Sans', sans-serif;
    text-align: start;
    font-size: 18px;
    color: #fff;
    padding: 5px;
    margin-top: 30px !important;
}
.card-text h6{
    font-family: 'Open Sans', sans-serif;
    text-align: start;
    font-size: 16px;
    font-weight: 300;
    color: #fff;
    padding: 5px;
}
.card-text ul{
    margin-top: 35px;
}
.card-text ul li{
    font-family: 'Open Sans', sans-serif;
    font-size: 16px;
    font-weight: 700;
    color: #fff !important;
    list-style: none;
    text-align: start;
    padding: 3px;
    margin-left: -30px;
}
.card-text ul li span{
    font-weight: 400;
    margin-left:5px;
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
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
}
.card img {
    width: 100%;
    height: auto;
    padding: 45px;
    border-top-left-radius: 25px;
    border-top-right-radius: 25px;
}
.fh5co-cta{
	background-image: url(https://www.delayflight24.com/uploads/airline/logo/2126/AIR_MALTA.png);
    height: 268px;
    opacity: 0.7;
}
.fh5co-cta-one{
	background-image: url(https://www.delayflight24.com/uploads/airline/logo/2126/AIR_MALTA.png);
    height: 268px;
    opacity: 0.7;
}
.fh5co-cta-two{
	background-image: url(https://www.delayflight24.com/uploads/airline/logo/2126/AIR_MALTA.png);
    height: 268px;
    opacity: 0.7;
}
.fh5co-cta-three{
	background-image: url(https://www.delayflight24.com/uploads/airline/logo/2126/AIR_MALTA.png);
    height: 268px;
    opacity: 0.7;
}
.fh5co-cta .overlay {
    background: rgba(250, 0, 0, 0.932);
    left: 0;
    right: 0;
    bottom: 0;
    top: 142px;
    position: absolute;
    z-index: -1;
    height: 268px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
}
.fh5co-cta-one .overlay {
    background: rgba(0, 38, 255, 0.87);
    left: 0;
    right: 0;
    bottom: 0;
    top: 142px;
    position: absolute;
    z-index: -1;
    height: 268px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
}
.fh5co-cta-two .overlay {
    background: rgba(0, 80, 18, 0.87);
    left: 0;
    right: 0;
    bottom: 0;
    top: 142px;
    position: absolute;
    z-index: -1;
    height: 268px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
}
.fh5co-cta-three .overlay {
    background: rgba(76, 0, 255, 0.87);
    left: 0;
    right: 0;
    bottom: 0;
    top: 142px;
    position: absolute;
    z-index: -1;
    height: 268px;
    border-bottom-left-radius: 25px;
    border-bottom-right-radius: 25px;
}
@media screen and (max-width: 768px) {
    .slider{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    .card-content{
        display: grid;
    }
}
</style>