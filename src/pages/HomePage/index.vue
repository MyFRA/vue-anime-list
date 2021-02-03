<template>
    <div>
        <Navbar />
       <div class="content">
            <Hero />
            <AnimeRow :headerTitle="'Trending Anime'"> 
                <Carousel :loop="true" :autoplay="true" :paginationEnabled="false">
                    <Slide v-for="anime in trending_anime" :key="anime.id">
                        <Anime :anime="anime"/>
                    </Slide>
                </Carousel>
            </AnimeRow>
            <AnimeRow :headerTitle="'Newest Anime'"> 
                <Carousel :loop="true" :autoplay="true" :paginationEnabled="false">
                    <Slide v-for="anime in newest_anime" :key="anime.id">
                        <Anime :anime="anime"/>
                    </Slide>
                </Carousel>
            </AnimeRow>
            <AnimeRow :headerTitle="'Anime Action'"> 
                <Carousel :loop="true" :autoplay="true" :paginationEnabled="false">
                    <Slide v-for="anime in anime_action" :key="anime.id">
                        <Anime :anime="anime"/>
                    </Slide>
                </Carousel>
            </AnimeRow>
       </div>
    </div>
</template>

<script>
import Navbar from '@/pages/HomePage/components/Navbar';
import Hero from '@/pages/HomePage/components/Hero';
import AnimeRow from '@/pages/HomePage/components/AnimeRow';
import Anime from '@/pages/HomePage/components/Anime';
import { Carousel, Slide } from 'vue-carousel';
import axios from 'axios';

export default {
    name: 'HomePage',
    data() {
        return {
            trending_anime: [],
            newest_anime: [],
            anime_action: [],
        }
    },
    components: {
        Navbar,
        Hero,
        AnimeRow,
        Carousel,
        Slide,
        Anime
    },
    created() {
        axios.get('https://kitsu.io/api/edge/trending/anime').then((res) => {
            this.trending_anime = res.data.data;
        });

        axios.get('https://kitsu.io/api/edge/anime?sort=-startDate').then((res) => {
            this.newest_anime = res.data.data;
        });

        axios.get('https://kitsu.io/api/edge/anime?filter[categories]=action').then((res) => {
            this.anime_action = res.data.data;
        });
    }
}
</script>

<style scoped>
    .content {
        padding: 0 1.5rem;
    }
</style>