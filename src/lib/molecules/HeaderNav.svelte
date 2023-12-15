<script>
    import { NavLogo, NavLink, BtnPrimary } from '$lib/index.js';
</script>

<nav>

    <NavLogo href="/"></NavLogo>

    <input class="menu-btn" type="checkbox" id="menu-btn" aria-label="Navigation menu" />
    <label class="menu-icon" for="menu-btn">
        <span class="navicon"></span>
    </label>

    <ul>
        <li>
            <NavLink href="/about" title="About"></NavLink>
        </li>
        <li>
            <NavLink href="/promise" title="Promise"></NavLink>
        </li>
        <li>
            <BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary>
        </li>
    </ul>


    <div class="area">
        <ul class="bubbels">

            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><BtnPrimary href="/becomeSponsor" title="Become sponsor"></BtnPrimary></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><NavLink href="/promise" title="Promise"></NavLink></li>
            <li><NavLink href="/about" title="About"></NavLink></li>
            <li><NavLink href="/promise" title="Promise"></NavLink></li>
        </ul>
    </div>





</nav>


<style>


    /* header */

    nav {
        background-color: var(--Bg-Dark-Blue);
        box-shadow: 1px 1px 4px 0 rgba(0,0,0,.1);
        position: fixed;
        width: 100%;
        z-index: 3;
        padding: 0 1em;
        min-width: 5rem;

    }

    nav ul {
        margin: 0;
        padding: 0;
        list-style: none;
        overflow: hidden;

        clear: both;
        max-height: 0;
        transition: max-height .2s ease-out;
    }

    nav li{
        padding: 5em 0;
        display: flex;
        justify-content: center;

    }

    nav li:nth-last-child(1){
        display: flex;
        justify-content: center;
    }

    /* Hamburger Menu */

    nav .menu-icon {
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        float: right;
        width: 3em;
        height: 3em;
        position: relative;
        top: 1.3em;
        right: 1em;
        user-select: none;
        background-color: var(--Yellow-Primary);
        border-radius: 50%;
    }

    nav .menu-icon .navicon {
        background: var(--Bg-Dark-Blue);
        display: block;
        height: 3px;
        position: relative;
        transition: background .2s ease-out;
        width: 24px;
    }

    nav .menu-icon .navicon:before,
    nav .menu-icon .navicon:after {
        background: var(--Bg-Dark-Blue);
        content: '';
        display: block;
        height: 100%;
        position: absolute;
        transition: all .2s ease-out;
        width: 100%;
    }

    nav .menu-icon .navicon:before {
        top: 5px;
    }

    nav .menu-icon .navicon:after {
        top: -5px;
    }

    /* menu btn */

    nav .menu-btn {
        display: none;
    }

    nav .menu-btn:checked ~ ul {
        max-height: 60em;
    }

    nav .menu-btn:checked ~ .menu-icon .navicon {
        background: transparent;
    }

    nav .menu-btn:checked ~ .menu-icon .navicon:before {
        transform: rotate(-45deg);
    }

    nav .menu-btn:checked ~ .menu-icon .navicon:after {
        transform: rotate(45deg);
    }

    nav .menu-btn:checked ~ .menu-icon:not(.steps) .navicon:before,
    nav .menu-btn:checked ~ .menu-icon:not(.steps) .navicon:after {
        top: 0;
    }

    /* 48em = 768px */

    @media (min-width: 48em) {

        nav ul{
            display: flex;
            align-items: center;
            padding: 0 3em;
            clear: none;
            float: right;
            max-height: none;
        }

        nav li {
            float: left;
            padding: 1em 0;
        }

        nav .menu-icon {
            display: none;
        }

    }

    .area {
    width: 100%;
    display: flex;
    justify-content: center;

    
}

.bubbels {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    list-style: none;
    padding: 0;
}

.bubbels li {
    position: absolute;
    display: inline-block;
    list-style: none;
    width: 100px;
    height: 100px;
    animation: animate 8s linear infinite;
    background-color: #ff65b7;
    bottom: -150px;
    border-radius: 50%;
    box-shadow: 0 0 10px rgba(255, 0, 150, 0.5);
    transform-origin: bottom center;
}

.bubbels li:nth-child(1) {
    left: 25%;
    background-color: #ff65b7;
}

.bubbels li:nth-child(2) {
    left: 10%;
    animation-delay: 1s;
    animation-duration: 10s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(3) {
    left: 70%;
    animation-delay: 2s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(4) {
    left: 40%;
    animation-delay: 1s;
    animation-duration: 15s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(5) {
    left: 65%;
    animation-delay: 2s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(6) {
    left: 75%;
    width: 120px;
    height: 120px;
    animation-delay: 3s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(7) {
    left: 35%;
    width: 180px;
    height: 180px;
    animation-delay: 4s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(8) {
    left: 50%;
    animation-delay: 2s;
    animation-duration: 20s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(9) {
    left: 20%;
    width: 140px;
    height: 140px;
    animation-delay: 3s;
    animation-duration: 18s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(10) {
    left: 85%;
    width: 250px;
    height: 250px;
    animation-delay: 0s;
    animation-duration: 8s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(11) {
    left: 35%;
    width: 250px;
    height: 250px;
    animation-delay: 2s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(12) {
    left: 50%;
    animation-delay: 1s;
    animation-duration: 12s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(13) {
    left: 20%;
    width: 120px;
    height: 120px;
    animation-delay: 3s;
    animation-duration: 15s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(14) {
    left: 85%;
    width: 250px;
    height: 250px;
    animation-delay: 0s;
    animation-duration: 8s;
    background-color: #ff65b7;
}
.bubbels li:nth-child(15) {
    left: 20%;
    width: 120px;
    height: 120px;
    animation-delay: 3s;
    animation-duration: 15s;
    background-color: #ff65b7;
}

.bubbels li:nth-child(16) {
    left: 85%;
    width: 250px;
    height: 250px;
    animation-delay: 0s;
    animation-duration: 8s;
    background-color: #ff65b7;
}

@keyframes animate {
    0% {
        transform: translateY(0px) rotate(0deg);
        opacity: 1;
        border-radius: 50%;
    }

    50% {
        transform: translateY(-500px) rotate(320deg);
        opacity: 1;
        border-radius: 50%;
    }

    100% {
        transform: translateY(-1000px) rotate(720deg);
        opacity: 1;
        border-radius: 50%;
    }
}





</style>