<template>
    <div class="card-youtube">
        <v-card-title class="cy-title"><span class="cyt-span">Que faisons nous ?</span></v-card-title>
        <iframe class="video" width="560" height="315" :src="embedUrl" title="YouTube video player" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
            allowfullscreen></iframe>
    </div>
</template>

<script>
export default {
    name: 'card-youtube',
    data() {
        return {
            videoId: 'j-wxTBml628'
        }
    },
    computed: {
        embedUrl() {
            return `https://www.youtube.com/embed/${this.videoId}`
        }
    },
    mounted() {

    },
    methods: {

    }
}

</script>

<style lang="scss">
.card-youtube{
    background-color: $primary-color;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    border-radius: 10px;
    border: solid 3px $tertiary-color;
    margin-bottom: 2%;
    padding-bottom: 2%;
}

.cy-title{
    font-family: 'Montserrat', sans-serif;
    font-size: 1.5rem;
    font-weight: 600;
    margin-bottom: 1rem;
}
.cyt-span{
     color: $tertiary-color;

}

@media (min-width: 760px) {
    .video {
        width: 700px;
    }
}

@media (max-width: 630px) {
    .video {
        width: 500px;
    }
}
@media (max-width: 560px) {
    .video {
        width: 400px;
    }
}
@media (max-width: 460px) {
    .video {
        width: 300px;
    }
}
// @media (max-width: 630px) {
//     .video {
//         width: 500px;
//     }
// }
// @media (max-width: 630px) {
//     .video {
//         width: 500px;
//     }
// }

</style>