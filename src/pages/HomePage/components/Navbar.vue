<template>
    <nav>
        <div class="hamburger">
            <div></div>
            <div></div>
            <div></div>
        </div>
        <div class="logo">
            <h3>
                <span>Wibu</span>
                <span>Stream.</span>
            </h3>
        </div>
        <div class="search-button">
            <i class="zmdi zmdi-search"></i>
        </div>
    </nav>
</template>

<style scoped>
    nav {
        width: 100%;
        height: 9vh;
        display: flex;
        align-items: center;
        justify-content: center;
        position: relative;
        background: #1A202C;
    }

    .hamburger {
        position: absolute;
        width: 30px;
        left: 1.5rem;
        cursor: pointer;
    }

    .hamburger div {
        background: #fff;
        width: 100%;
        height: 3px;
        margin: 4px 0;
        border-radius: 10px;
    }

    .hamburger div:nth-child(2) {
        width: 85%;
    }

    .hamburger div:nth-child(3) {
        width: 70%;
    }

    .logo {
        width: 100%;
        text-align: center;
    }

    .logo h3 span:first-child {
        color: #fff;
    }

    .logo h3 span:last-child {
        color:  #295EC4;
    }

    .search-button {
        position: absolute;
        right: 1.5rem;
        color: #fff;
        width: 30px;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
    }

    .search-button i {
        font-size: 25px;
    }
</style>