<script setup>
const footerContent = {
    footerDetails: {
        contactDetails: [
            {contactTitle: 'Phone :' , contactInfo: '02226603034'},
            {contactTitle: 'Whatsapp :' , contactInfo: '01727-985581'},
            {contactTitle: 'E-mail :' , contactInfo: 'sales@siyamholidays.com'},
        ],

        logoSrc: "/assets/logo_2-672de651.png",
        hotlineNumber: ' 0188 00 78 901',

        socialContact: [
            {icon: 'fab fa-facebook-f' , name: 'Facebook', socialLink: '#'},
            {icon: 'fab fa-twitter' , name: 'Twitter', socialLink: '#'},
            {icon: 'fa-brands fa-instagram' , name: 'Instagram', socialLink: '#'},
            {icon: 'fa-brands fa-linkedin-in' , name: 'Linkedin', socialLink: '#'},
            {icon: 'fab fa-youtube' , name: 'YouTube', socialLink: '#'},
            {icon: 'fa-brands fa-tiktok' , name: 'TikTok', socialLink: '#'},
        ]
    },
}
const offices = [
    {
        branch: 'Bangladesh Office',
        name: 'Siyam Holidays',
        email: 'siyaminfo@gmail.com',
        phoneNumber: '+880 1880 078901',
        address: 'House#62, Road#15, Block-C, Banani, Dhaka-1212, Bangladesh. Contact: 09639888555'
    },
    {
        branch: 'Dubai Office',
        name: 'Siyam Holidays Tourism L.L.C',
        email: 'siyaminfo@gmail.com',
        phoneNumber: '+971 1854 39547',
        address: 'Bin Zafar Building, Shop No-03, Eyal Nasser, Deira, Naif, Dubai, United Arab Emirates.'
    },
    {
        branch: 'Thailand Office',
        name: 'Siyam Holidays Co, Ltd',
        email: 'siyaminfo@gmail.com',
        phoneNumber: '+66 10 012000',
        address: '21/34, Moo-5, Nangprue Banglamung, Chonburi-20150, Thailand.'
    }
]
</script>

<template>
      
      <section class="footer_area">
        <footer class="row print">
                <div class="footertop">
                    
                    <div class="container mt-3">
                        <div class="row">
                            <div class="col-md-3 col-sm-6" style="color: white;font-weight: normal;font-size: 15px;">
                                <div class="">
                                    <img :src="footerContent.footerDetails.logoSrc" alt="" style="width: 200px; margin-bottom: 7px;">
                                </div> 
                                <p v-for="(contact , index) in footerContent.footerDetails.contactDetails" :key="index" class="">
                                    {{ contact.contactTitle }} {{ contact.contactInfo }}
                                </p>

                                <h3 class="contact" >24<span class=" " style="color: #fd9604;">/</span>7 Contact </h3>
                                <h5 class="number" style="color: #fd9604;">{{ footerContent.footerDetails.hotlineNumber }}</h5>
                                    <div class="col-md-12 padding" style="margin-top: 10px;margin-bottom: 10px;">
                                        <img src="https://tvlk.imgix.net/imageResource/2017/12/13/1513150313470-072f6bdc02c0b73fcf791aa2b2264fbd.svg?auto=compress%2Cformat&cs=srgb&ixlib=java-1.1.12&q=75" style="width: 80px;">
                                         <img src="https://tvlk.imgix.net/imageResource/2017/12/13/1513150321127-5096be77d2a19401b476853e54ba2cc6.svg?auto=compress%2Cformat&cs=srgb&ixlib=java-1.1.12&q=75" style="width: 80px;">
                                         <img src="http://siyamholidays.com/images/tat.png" style="width: 200px;margin-top: 10px;">
                                    </div>
                            </div>

                            <div class="col-md-3 col-sm-6 padding">
                                <h6 class="heading7"> About Us </h6>
                                <ul class="footer-ul" style="font-weight: normal;">
                                    <li><a href="#"> How to Book </a></li>
                                    <li><a href="#"> Contact Us </a></li>
                                    <li><a href="#"> Help Center </a></li>
                                    <li><a href="#"> About Us </a></li>
                                    <li> 
                                        <h3 class="mt-3" style="color: white; font-size: 20px; font-weight: 500; letter-spacing: 0.2px;"> Follow <span class=" " style="color: #fd9604;">US</span> on </h3>
                                    </li>

                                    <li v-for="(social , index) in footerContent.footerDetails.socialContact" :key="index">
                                        <a :href="social.socialLink" target="_blank" class="Link">
                                            <i :class="social.icon"></i>
                                            {{ social.name }}
                                        </a>
                                    </li>
                                    <!-- <li>
                                        <a href="https://twitter.com/" class="color-white">
                                            <i class="fab fa-twitter"></i> 
                                            Twitter
                                        </a>
                                    </li>
                                    <li>
                                        <a href="https://www.youtube.com">
                                            <i class="fab fa-youtube"></i> Youtube
                                        </a>
                                    </li> -->
                                </ul>
                            </div>

                            <div class="col-md-3 col-sm-6">
                                <h6 class="heading7"> Products </h6>
                                <ul class="footer-ul" style="font-weight: normal;">
                                    <li><a href="#"> Hotels </a></li>
                                    <li><a href="#"> Flight </a></li>
                                    <li><a href="#"> Package Tour</a></li>
                                    <li><a href="#"> Transportation </a></li>
                                    <li><a href="#"> Attractions & Activities </a></li>
                                    <li><a href="#"> Visa Service </a></li>
                                    <li><a href="#"> Hajj </a></li>
                                    <li><a href="#"> Umrah </a></li>
                                </ul>
                            </div>

                            <div class="col-md-3 col-sm-6">
                                <h6 class="heading7"> Others </h6>
                                <ul class="footer-ul" style="font-weight: normal;">
                                    <li><a href="subscription.php"> Newsletter Subscription</a></li>
                                    <li><a href="privacypolicy.php"> Privacy Policy</a></li>
                                    <li><a href="terms.php"> Terms &amp; Conditions</a></li>
                                   <!--  <li><a href="#">Register Your Hotel</a></li> -->
                                   <!--  <li><a href="#"> Vendor Partner </a></li> -->
                                    <li><a href="travelagent.php"> Travel Agent </a></li>
                                    <li><a href="#"> <img src="http://siyamholidays.com/images/pay.png" alt="" style="width: 180px; margin-top: 10px;"> </a></li>
                                </ul>
                            </div>
                        </div>
                    </div>

                    <!----------secend stap start---------->

                    <div class="container secend-area">
                        <div class="row">
                            <div class="col-md-4" v-for="(office, index) in offices" :key="index">
                                <div class="col-md-12 secend-box">
                                    <h4 class=" mt-2 Branch">{{ office.branch }}</h4>
                                    <hr>
                                    <h4 class="Office_Name">{{ office.name }}</h4>
                                    <h4 class="Contact">{{ office.email }}</h4>
                                    <h4 class="Contact">{{ office.phoneNumber }}</h4>
                                    <p class="p Address">{{ office.address }}</p>
                                </div>
                            </div>
                        </div>
                    </div>
                    <!----------secend stap End---------->
                </div>
        </footer>

      </section>
    
</template>

<style scoped>
.footer_area {
    width: 100%;
    padding: 20px;
    background: black;
    overflow: hidden;
}

.footer-ul {
    margin-top: 20px;
    color: white;
    list-style: none;
    padding: 0;
}

.footer_area ul li a {
    font-size: 14px;
    line-height: 25px;
    text-decoration: none;
    color: white; 
}

svg:not(:root).svg-inline--fa {
    overflow: visible;
    color: #fd9604;
    font-size: 18px;
    margin: 0px 5px;
}
.Link i{
    color: #fd9604;
    font-size: 18px;
    margin: 5px 7px;
}
.heading7 {
    color: #fd9604;
    font-size: 20px;
    font-weight: 700;
}

.contact {
    color: white;
    font-size: 20px;
    font-weight: 600;
    letter-spacing: 0.2px;
}

.number {
    color: white;
    font-size: 16px;
}

hr:not([size]) {
    height: 2px;
}

hr {
    background-color: #8cd02c;
    margin: 10px auto;
}

.secend-area {
    border-radius: 10px;
}

.secend-box {
    border-radius: 10px;
    border: 1px solid #fd9604;
    padding: 10px;
    margin-top: 20px;
}

/* .secend-box h4 {
    margin-left: 0;
    font-size: 16px;
} */

.secend-box p {
    font-size: 14px;
    margin-left: 0;
}
.Branch{
    text-align: center; 
    font-size: 20px; 
    color: #fd9604;
}
.Office_Name{
    color: white; 
    font-size: 18px;
}
.Address{
    font-size: 14px;
    line-height: 1.6;
    color: white;
    font-weight: normal;
}
.Contact{
    font-size: 16px;
    line-height: 0.5;
    color: #8d8d8d;
}
@media screen and (max-width: 768px) {
    .footer_area {
        padding: 15px;
    }

    .footer_area ul li a,
    .heading7,
    .contact,
    .number {
        font-size: 16px;
    }
    .heading7{
        font-size: 20px;
        margin-left: 0px;
    }

    svg:not(:root).svg-inline--fa {
        font-size: 16px;
    }

    .secend-box h4 {
        font-size: 14px;
    }

    .secend-box p {
        font-size: 12px;
    }
}

</style>