<script setup>
const headerContent = {
    contactInfo: {
        address: "1010 Avenue, New York, NY 10018 US.",
        phoneNumber: "212 386 5575, 212 386 5576",
        hours: "Mon-Sat, 8.00-18.00. Sunday CLOSED"
    },
    navbarContent: {
        logoSrc: "../../assets/img/Travel/Logo/logo_2.png",
        navItems: [
            { label: "Home", link: "/" },
            { label: "Hotel", link: "/hotel" },
            { label: "Package Tour", link: "/package-tour" },
            {
                label: "Transportation",
                dropdownItems: [
                    { label: "Flight", link: "/flight" },
                    { label: "By Road", link: "/transportation" }
                ]
            },
            { label: "Sightseeing", link: "/activites" },
            { label: "Visa", link: "/visa" }
        ],
        loginButtonLink: "#"
    }
};

</script>

<template>
    
    <div class="bg-primary py-3 d-none d-sm-block text-white fw-bold">
        <div class="container">
            <div class="row align-items-center gx-4">
                <div class="col-auto d-none d-lg-block fs--1">
                    <span class="fas fa-map-marker-alt text-warning me-2" data-fa-transform="grow-3"></span>
                        {{ headerContent.contactInfo.address }}
                </div>
                <div class="col-auto ms-md-auto order-md-2 d-none d-sm-flex fs--1 align-items-center">
                    <span class="fas fa-clock text-warning me-2" data-fa-transform="grow-3"></span>
                    {{ headerContent.contactInfo.phoneNumber }}
                </div>
                <div class="col-auto">
                    <span class="fas fa-phone-alt text-warning" data-fa-transform="shrink-3"></span>
                    <a class="ms-2 fs--1 d-inline text-white fw-bold" href="tel:2123865575">
                        {{ headerContent.contactInfo.hours }}
                    </a>
                </div>
            </div>
      </div>
    </div>
    <div class="sticky-top navbar-elixir">
        <div class="container">
            <nav class="navbar navbar-expand-lg"> 
                <a class="navbar-brand" href="/">
                    <img :src="headerContent.navbarContent.logoSrc" alt="logo" class="nav-logo" />
                </a>
                <button class="navbar-toggler p-0" type="button" data-bs-toggle="collapse" data-bs-target="#primaryNavbarCollapse" aria-controls="primaryNavbarCollapse" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="hamburger hamburger--emphatic">
                        <span class="hamburger-box"><span class="hamburger-inner"></span></span>
                    </span>
                </button>
                <div class="collapse navbar-collapse" id="primaryNavbarCollapse">
                    <ul class="navbar-nav py-3 py-lg-0 mt-1 mb-2 my-lg-0 ms-lg-n1">
                        <template v-for="(navItem, index) in headerContent.navbarContent.navItems">
                            <li v-if="!navItem.dropdownItems" :key="index" class="nav-item">
                                <RouterLink class="nav-link" :to="navItem.link" role="button">{{ navItem.label }}</RouterLink>
                            </li>
                            <li v-else :key="navItem" class="nav-item dropdown">
                                <a class="nav-link dropdown-toggle dropdown-indicator" href="JavaScript:void(0)" role="button" data-bs-toggle="dropdown" aria-expanded="false">{{ navItem.label }}</a>
                                <ul class="dropdown-menu">
                                    <li v-for="(dropdownItem, dIndex) in navItem.dropdownItems" :key="dIndex">
                                        <RouterLink class="dropdown-item" :to="dropdownItem.link" role="button">{{ dropdownItem.label }}</RouterLink>
                                    </li>
                                </ul>
                            </li>
                        </template>
                    </ul>
                    <a class="btn btn-outline-primary rounded-pill btn-sm border-2 d-block d-lg-inline-block ms-auto my-3 my-lg-0" :href="headerContent.navbarContent.loginButtonLink" target="_blank">Login</a>
                </div>
            </nav>
      </div>
    </div>

</template>

<style scoped>
.dropdown:hover.dropdown-menu {
    display: block;
}

.btn-outline-primary:active{
    background: none !important;
}
.navbar-brand{
    width: 25%;
}
.navbar-brand img{
    max-width: 55%;
}
@media screen and (max-width: 768px) {
    .navbar-brand{
        width: 50%;
    }
    .navbar-brand img{
    max-width: 100%;
    }
}
</style>