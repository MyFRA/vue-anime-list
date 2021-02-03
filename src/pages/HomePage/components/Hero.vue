<template>
    <div class="hero" ref="hero">
        <div class="inner">
            <div class="text">
                <h3 class="title">Attack On Titan (2013)</h3>
                <div class="rating">
                    <span><i class="zmdi zmdi-star" style="color: #D39D33"></i> 8.8</span>
                    <span>/ 10 IMDb</span>
                </div>
                <div class="episodes">
                    <span>63 Episodes <i class="zmdi zmdi-circle"></i> Japanese & English</span>
                </div>
            </div>
            <div class="controls-wrapper">
                <input type="radio" name="hero">
                <input type="radio" name="hero">
                <input type="radio" name="hero">
                <input type="radio" name="hero">
            </div>
        </div>
    </div>
</template>

<script>

export default {
    mounted() {
        this.$refs.hero.style.height = this.$refs.hero.offsetWidth + 'px';
    },
}
</script>

<style scoped>
    .hero {
        width: 100%;
        background-image: url('https://i.pinimg.com/564x/47/7f/1d/477f1dc366006ab7fb8d304ed59677ec.jpg');
        background-size: cover;
        background-position: center;
        border-radius: 20px;
        margin-top: .4rem;
    }

    .hero .inner {
        width: 100%;
        height: 100%;
        background: rgb(0,0,0);
        background: linear-gradient(0deg, rgba(0,0,0,1) 0%, rgba(255,255,255,0) 100%);
        border-radius: 20px;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        color: #ddd;
        padding: .8rem 1rem;
    }

    .hero .inner .text {
        margin-bottom: 1.7rem;
    }

    .hero .inner .text .title {
        font-size: 23px;
        margin-bottom: 4px;
    }

    .hero .inner .text .rating {
        margin-bottom: 6px;
        font-size: 14px;
    }

    .hero .inner .text .episodes {
        font-size: 14px;
    }

    .hero .inner .controls-wrapper {
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .hero .inner .controls-wrapper input[type="radio"] {
        margin: 0 3px;
    }

</style>