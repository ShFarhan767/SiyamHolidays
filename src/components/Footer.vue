<script setup>

const FooterContent = {
    FooterLogo: {
        image: "../../assets/img/Header.png",
    },
    ContactInfo: {
        Phone: "Phone: 02226603034",
        Whatsapp: "Whatsapp : 01727-985581",
        Email: "E-mail: sales@siyamholidays.com",
    },
    Contact: {
        towntyFor: "24",
        Saven: "7 Contact",
        Number: "0188 00 78 901",
    },
    FooterImage: {
        image: "http://siyamholidays.com/images/tat.png",
    },
    AboutHeading: {
        AboutTitle: "About Us",

    },
    About: [
        { List: "How to Book" },
        { List: "Contact Us" },
        { List: "Help Center" },
        { List: "About Us" },
    ],
    Follow: [
        { List: "fab fa-facebook-f", IconName: "Facbook" },
        { List: "fab fa-twitter", IconName: "Twitte" },
        { List: "fab fa-google-plus-g", IconName: "Google plus" },
        { List: "fab fa-youtube", IconName: "Youtube" },

    ],
    ProductsInfo: {
        ProductsTaitle: "Products",
    },
    Products: [
        { List: "Hotels" },
        { List: "Flight" },
        { List: "Package Tour" },
        { List: "Transportation" },
        { List: "Attractions & Activities" },
        { List: "Visa Service" },
        { List: "Hajj" },
        { List: "Umrah" },
    ],
    Otherinfo: {
        OthersTitle: "Others",
    },
    other: [
        { list: "Newsletter Subscription" },
        { list: "Privacy Policy" },
        { list: "Terms &amp; Conditions" },
        { list: "Travel Agent" },
    ],
    OtherImage: {
        image: "http://siyamholidays.com/images/pay.png"
    },
    secentBox1: {
        Title: "Bangladesh Office",
        Office: "Siyam Holidays",
        Location: "House#62, Road#15, Block-C, Banani, Dhaka-1212, Bangladesh.Contact: 09639888555"
    },
    secentBox2: {
        Title: "Dubai Office",
        Office: "Siyam Holidays Tourism L.L.C",
        Location: "Bin Zafar Building, Shop No-03, Eyal Nasser, Deira, Naif, Dubai, United Arab Emirates."
    },
    secentBox3: {
        Title: "Thailand Office",
        Office: "Siyam Holidays Co, Ltd",
        Location: "21/34, Moo-5, Nangprue Banglamung, Chonburi-20150, Thailand. "
    },
}

</script>

<template>
    <section class="footer_area">
        <footer class="row print">
            <div class="footertop">

                <div class="container mt-3">
                    <div class="row">
                        <div class="col-md-3 col-sm-6" style="color: white;font-weight: normal;font-size: 15px;">
                            <div class=""><img :src="FooterContent.FooterLogo.image" alt=""
                                    style="width: 200px; margin-bottom: 7px;"></div>
                            <p class="">
                                {{ FooterContent.ContactInfo.Phone }}
                            </p>

                            <p class="">
                                {{ FooterContent.ContactInfo.Whatsapp }}
                            </p>
                            <p class="">
                                {{ FooterContent.ContactInfo.Email }}
                            </p>

                            <h3 class="contact">{{ FooterContent.Contact.towntyFor }}<span class=" "
                                    style="color: #fd9604;">/</span>{{ FooterContent.Contact.Saven }} </h3>
                            <h5 class="number" style="color: #fd9604;">{{ FooterContent.Contact.Number }}</h5>
                            <div class="col-md-12 padding" style="margin-top: 10px;margin-bottom: 10px;">
                                <img src="https://tvlk.imgix.net/imageResource/2017/12/13/1513150313470-072f6bdc02c0b73fcf791aa2b2264fbd.svg?auto=compress%2Cformat&cs=srgb&ixlib=java-1.1.12&q=75"
                                    style="width: 80px;">
                                <img src="https://tvlk.imgix.net/imageResource/2017/12/13/1513150321127-5096be77d2a19401b476853e54ba2cc6.svg?auto=compress%2Cformat&cs=srgb&ixlib=java-1.1.12&q=75"
                                    style="width: 80px;">
                                <img :src="FooterContent.FooterImage.image" style="width: 200px;margin-top: 10px;">
                            </div>
                        </div>

                        <div class="col-md-3 col-sm-6 padding">
                            <h6 class="heading7"> {{ FooterContent.AboutHeading.AboutTitle }} </h6>
                            <ul class="footer-ul" style="font-weight: normal;">
                                <li v-for="(Abouts, index) in FooterContent.About" :key="index"><a
                                        href="#">{{ Abouts.list }}</a></li>
                                <li>
                                    <h3 class="mt-3"
                                        style="color: white; font-size: 20px; font-weight: 500; letter-spacing: 0.2px;">
                                        Follow <span class=" " style="color: #fd9604;">US</span> on </h3>
                                </li>

                                <li v-for="(Follows, index) in FooterContent.Follow" :key="index"><a
                                        href="https://www.facebook.com/siyamholidays/" target="_blank"
                                        class="color-white"><i :class="Follows.List"></i>{{ Follows.IconName }}</a></li>

                            </ul>
                        </div>

                        <div class="col-md-3 col-sm-6">
                            <h6 class="heading7"> {{ FooterContent.ProductsInfo.ProductsTaitle }} </h6>
                            <ul class="footer-ul" style="font-weight: normal;">
                                <li v-for="(productss, index) in FooterContent.Products" :key="index"><a href="#">
                                        {{ productss.List }} </a></li>
                            </ul>
                        </div>

                        <div class="col-md-3 col-sm-6">
                            <h6 class="heading7"> {{ FooterContent.Otherinfo.OthersTitle }} </h6>
                            <ul class="footer-ul" style="font-weight: normal;">
                                <li v-for="(otherss, index) in FooterContent.other" :key="index"><a
                                        href="subscription.php">{{ otherss.list }}</a></li>
                                <!-- <li><a href="privacypolicy.php"> </a></li>
                                    <li><a href="terms.php"></a></li> -->
                                <!--  <li><a href="#">Register Your Hotel</a></li> -->
                                <!--  <li><a href="#"> Vendor Partner </a></li> -->
                                <!-- <li><a href="travelagent.php"> </a></li> -->
                                <li><a href="#"> <img :src="FooterContent.OtherImage.image" alt=""
                                            style="width: 180px; margin-top: 10px;"> </a></li>
                            </ul>
                        </div>
                    </div>
                </div>

                <!----------secend stap start---------->

                <div class="container secend-area">
                    <div class="row">
                        <div class="col-md-4 ">
                            <div class="col-md-12 secend-box">
                                <h4 class=" mt-2" style="text-align: center; font-size: 18px; color: #fd9604;">{{
                                    FooterContent.secentBox1.Title }}</h4>
                                <hr>
                                <h4 style="color: white; font-size: 16px;"> {{ FooterContent.secentBox1.Office }} </h4>
                                <p class="p" style="color: white;font-weight: normal;">{{ FooterContent.secentBox1.Location
                                }}</p>
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="col-md-12 secend-box">
                                <h4 class="mt-2" style="text-align: center;color: white;font-size: 18px;color: #fd9604;">{{
                                    FooterContent.secentBox2.Title }}</h4>
                                <hr>
                                <h4 style="color: white; font-size: 16px;"> {{ FooterContent.secentBox2.Office }} </h4>
                                <p class="p" style="color: white;font-weight: normal;">{{ FooterContent.secentBox2.Location
                                }}</p>
                            </div>
                        </div>
                        <div class="col-md-4">
                            <div class="col-md-12 secend-box">
                                <h4 class="mt-2" style="text-align: center;color: white; font-size: 18px;color: #fd9604;">{{
                                    FooterContent.secentBox3.Title }}</h4>
                                <hr>
                                <h4 style="color: white; font-size: 16px;">{{ FooterContent.secentBox3.Office }}</h4>
                                <p class="p" style="color: white;font-weight: normal;">{{ FooterContent.secentBox3.Location
                                }}</p>
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

.secend-box h4 {
    margin-left: 0;
    font-size: 16px;
}

.secend-box p {
    font-size: 14px;
    margin-left: 0;
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

    .heading7 {
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
}</style>