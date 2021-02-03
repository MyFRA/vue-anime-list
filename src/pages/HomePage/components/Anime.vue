<template>
    <router-link to="/5">
        <div class="anime">
            <div class="cover" v-bind:style="{'background-image': `url('${anime.attributes.posterImage.original}')`}">
            </div>
            <div class="anime-small-wrapper">
                <h4 class="title">{{ anime.attributes.titles.en }}</h4>
                <div class="rating">
                    <i class="zmdi zmdi-star"></i>
                    <span>
                        7.9 / 10 IMDb
                    </span>
                </div>
            </div>
        </div>
    </router-link>
</template>

<script>
export default {
    props: ['anime'],
    data() {
        return {
            cover: 'https://i1.wp.com/doublesama.com/wp-content/uploads/2018/04/Boruto-cover.png'
        }
    }
}
</script>

<style scoped>
    .anime {
        display: flex;
        flex-direction: column;
        margin: 0 .7rem;
    }

    .cover {
        height: 200px;
        background-size: cover;
        background-position: center;
        border-radius: 6px;
    }

    .rating {
        color: red;
    }

    h4.title {
        color: #fff;
        font-weight: 500;
        font-size: 14px;
        margin-top: 12px;
    }

    .rating {
        margin-top: 7px;
        color: #fff;
        display: flex;
        align-items: center;
    }

    .rating i {
        color: #D39D32;
        margin-right: 6.5px;
    }

    .rating span {
        font-size: 13px;
    }

    .anime-small-wrapper {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    a {
        text-decoration: none !important;
    }
</style>