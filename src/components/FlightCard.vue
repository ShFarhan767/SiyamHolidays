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
        email: 'airmaltaserv@gmail.com'
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
        email: 'airmaltaserv@gmail.com'
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
        email: 'airmaltaserv@gmail.com'
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
        email: 'airmaltaserv@gmail.com'
    }
];

</script>

<template>
    <div class="container Flight-Card">
        <div class="row">
            <h2>Feature Flight</h2>
                <div class="card-content">
                    <!-- Card -->
                    <div class="card" v-for="(airline, index) in airlines" :key="index">
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
                    </div>
                    <!-- Card End -->

                        
                </div>

        </div>
    </div>
</template>

<style scoped>
.Flight-Card{
    margin-top: 100px;
}
.Flight-Card h2{
    text-align: center;
    font-family: 'Fira Sans', sans-serif;
    color: #fd9604;
    letter-spacing: 0.5px;
    font-size: 48px;
    padding: 15px;
}
.card-content{
    margin-top: 50px;
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
    box-shadow: 2px 2px 20px rgba(0, 0, 0, 0.3);
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
    margin-left: -15px;
}
.card-text h6{
    font-family: 'Open Sans', sans-serif;
    text-align: start;
    font-size: 16px;
    font-weight: 300;
    color: #fff;
    padding: 5px;
    margin-left: -15px;
}
.card-text ul{
    margin-top: 35px;
    margin-left: -25px;
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
  .Flight-Card h2{
    font-size: 38px;
  }
  .card{
    margin: 45px;
  }
}
</style>