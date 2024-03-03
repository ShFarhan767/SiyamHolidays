<script setup>
const offerContent = {
    firstCard: {
        imageSrc: 'https://static.vecteezy.com/system/resources/previews/011/665/099/original/stylized-3d-discount-badge-illustration-for-black-friday-sale-free-png.png',
        code: 'WELCOMESS',
        discount: 40,
        description: 'on Your 1ST Booking',
        details: 'of Flight, Hotels and more',
        link: '#' // Add your offer link here
    },
    secondCard: {
        imageSrc: 'https://static.vecteezy.com/system/resources/previews/011/665/099/original/stylized-3d-discount-badge-illustration-for-black-friday-sale-free-png.png',
        title: 'Travel Insurance',
        description: 'No Worrying When Travel',
        details: 'Choose Our Best Insurance',
        link: '#' // Add your offer link here
    },
    thirdCard: {
        imageSrc: 'https://www.pngall.com/wp-content/uploads/8/Tour-PNG-Download-Image.png',
        code: 'WELCOMESS',
        discount: 40,
        description: 'on Your 1ST Booking',
        details: 'of Flight, Hotels and more',
        link: '#' // Add your offer link here
    },
};
</script>

<template>

    <section class="offer-area">
        <div class="container">
            <div class="row">
                <div class="col-md-4 offer-box" style="margin-left: -10px;">
                    <div class="col-md-2">
                        <img :src="offerContent.firstCard.imageSrc" alt="">
                    </div>
                    <div class="col-md-8" style="float: left;">
                        <p class="offer-p">Use Code: {{ offerContent.firstCard.code }}</p> <br>
                        <h5 class="updescount">UP TO <span class="" style="color: #fd9604;"> {{ offerContent.firstCard.discount }}% OFF</span> </h5>
                        <h6 class="Booking">{{ offerContent.firstCard.description }}</h6>
                        <p class="Flight">{{ offerContent.firstCard.details }}</p>
                    </div>

                    <div class="col-md-2" style="float: left;">
                        <a :href="offerContent.firstCard.link" class=""><i class="fas fa-arrow-right"></i></a>
                    </div>
                        
                </div>
                <div class="col-md-4 offer-box1" style="margin-left: 5px;">
                    <div class="col-md-2">
                        <img :src="offerContent.secondCard.imageSrc" alt="">
                    </div>
                    <div class="col-md-8" style="float: left;">
                        <p class="offer-p" style="font-size: 18px; font-weight: 600;">{{ offerContent.secondCard.title }}</p> <br>
                        <h5 class="updescount"></h5>
                        <h6 class="Booking">{{ offerContent.secondCard.description }}</h6>
                        <p class="Flight">{{ offerContent.secondCard.details }}</p>
                    </div>

                    <div class="col-md-2" style="float: left;">
                        <a :href="offerContent.secondCard.link" class=""><i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>


                <div class="col-md-4 offer-box2" style="margin-left: 5px;">
                    <div class="col-md-2">
                        <img :src="offerContent.thirdCard.imageSrc" alt="">
                    </div>
                    <div class="col-md-8" style="float: left;">
                        <p class="offer-p">Use Code: {{ offerContent.thirdCard.code }}</p> <br>
                        <h5 class="updescount">UP TO <span class="" style="color: #fd9604;"> {{ offerContent.thirdCard.discount }}% OFF</span> </h5>
                        <h6 class="Booking">{{ offerContent.thirdCard.description }}</h6>
                        <p class="Flight">{{ offerContent.thirdCard.details }}</p>
                    </div>

                    <div class="col-md-2" style="float: left;">
                        <a :href="offerContent.thirdCard.link" class=""><i class="fas fa-arrow-right"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

</template>

<style scoped>
.offer-area{
    width: 100%;
    height: auto;
    background: #ecebeb;
}
.offer-box{
    border: 1px solid #fd9604;
    border-radius: 10px;
     background: linear-gradient( to left, #af2424,#f12166);
}
.offer-box img{
    width: 80px;
    height: 80px;
    margin-top: 30px;
    float: left;
}
.offer-p{
    color: #fff;
    margin-top: 55px;
    margin-left: 15px;
    float: left;
    font-size: 16px;
}
.updescount{
    color: #fff;
    font-size: 18px;
    margin-top: -10px;
    margin-left: 15px;
    float: left;
}
.updescount span{
    font-size: 22px;
}
.Booking{
    font-size: 16px;
    color: #fff;
    margin-left: 15px;
    float: left;
}
.Flight{
    float: left;
    color: #fff;
    margin-left: 15px;
}
.offer-box a{
    font-size: 20px;
    border-radius: 50%;
    margin-left: 26%;
    top: 20px;
    position: absolute;
    padding: 7px 12px;
    background: #fd9604;
    color: #fff;
}
.offer-box1 a {
    font-size: 20px;
    border-radius: 50%;
    margin-left: 26%;
    top: 20px;
    position: absolute;
    padding: 7px 12px;
    background: #fd9604;
    color: #fff;
}
.offer-box2 a {
    font-size: 20px;
    border-radius: 50%;
    margin-left: 26%;
    top: 20px;
    position: absolute;
    padding: 7px 12px;
    background: #fd9604;
    color: #fff;
}
.offer-box1{
    border: 1px solid #fd9604;
    border-radius: 10px;
    gap: 10px;
    background: linear-gradient( to left, #91af24,#5fbd34);
}
.offer-box1 img{
    width: 90px;
    height: 90px;
    margin-top: 20px;
    float: left;
}
.offer-box2{
    border: 1px solid #fd9604;
    border-radius: 10px;
    background: linear-gradient( to left, #35b91a,rgb(30, 104, 216));
}
.offer-box2 img{
    width: 95px;
    height: 85px;
    margin-top: 30px;
    float: left;
}
@media screen and (max-width: 768px) {
    .offer-box1{
        margin-top: 20px;
    }
    .offer-box2{
        margin-top: 20px;
    }
}
</style>