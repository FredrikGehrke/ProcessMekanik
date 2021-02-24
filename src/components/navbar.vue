<template>

    <nav class="stroke navbar fixed-top scrolling-navbar navbar-expand-lg my-nav-color">
        <div class="container">
            <a class="navbar-brand" href="http://processmekanik.se/">
                <h4 class="mb-0 logo">ProcessMekanik</h4>
            </a>
            <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav"
                aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"><i id="my-toggler-icon" class="fas fa-bars my-color"></i></span>
            </button>
                <div class="collapse navbar-collapse" id="navbarNav">
                    <ul class="navbar-nav ml-2 min-font">
                        <li class="nav-item" data-toggle="collapse" data-target=".navbar-collapse.show">
                            <a class="nav-link waves-effect waves-light" href="#tjanster">Tjänster</a>
                        </li>
                        <li class="nav-item" data-toggle="collapse" data-target=".navbar-collapse.show">
                            <a class="nav-link waves-effect waves-light" href="#referenser">Referenser</a>
                        </li>
                        <li class="nav-item" data-toggle="collapse" data-target=".navbar-collapse.show">
                            <a class="nav-link waves-effect waves-light" href="#kontakt">Kontakt</a>
                        </li>
                    </ul>
                </div>
            <a id="mail-icon" href="mailto:thomas.claesson@processmekanik.se"><i class="fas fa-envelope fa-2x my-color px-2"></i></a>
        </div>
        <div class="elfsight-app-10f96e3d-63af-4ae4-bab5-4c10d2a875fb"></div>
    </nav>

</template>

<style scoped>

.logo {
    color: #2979ff;
}

.my-nav-color {
    background: rgba(32, 32, 32, 0.555);
}

#my-toggler-icon {
    background-color: var(--theme-color);
    color: white;
}

.nav-link {
    letter-spacing: 1px;
    font-size: 18px;
    color: white;
}

.nav-link:active {
    color: var(--theme-color);
    background-color: none;
}

#nav-Logo {
    width: 100%;
    max-width: 37px;
    height: auto;
}

#my-toggler-icon {
    padding: 5px 8px 5px 8px;
    border-radius: 5px;
    border: 1px solid var(--theme-color);
}

/* MEDIA QUERIES */
@media(max-width: 992px) { 

    #mail-icon {
        display: none;
    }

    #instagram-icon {
        display: none;
    }
}

@media(min-width: 992px) { 

    /* stroke */
    nav.stroke ul li a,
    nav.fill ul li a {
        position: relative;
    }
    nav.stroke ul li a:after,
    nav.fill ul li a:after {
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        margin: auto;
        width: 0%;
        content: '.';
        color: transparent;
        background: #00C851;
        height: 3px;
    }
    nav.stroke ul li a:hover:after {
        width: 80%;
        background: var(--theme-color);
        box-shadow: 0px 0px 20px 2px var(--theme-color);  
        border-radius: 100px;
        transition: all 0.6s;
        opacity: 90%;
    }
}

@media(min-width: 100000px) { 

    .waves-effect {
        position: relative;
        overflow: hidden;
        cursor: pointer;
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
        -webkit-tap-highlight-color: transparent;
    }

    a.waves-effect, a.waves-light {
    display: inline-block;
}
}
</style>