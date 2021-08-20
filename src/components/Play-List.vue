<template>
    <div>
        <h1>Music Playlist:</h1>
        <ol>
            <SongComp
                v-for="(song, index) in songs"
                :key="song.title"
                :songMetaData="song"
                :buttonLabel="'Remove'"
                :addSong="() => $emit('addtoPlaylist', index)"
                />
        </ol>
    </div>
</template>

<script>
import SongComp from './Song-Comp.vue'
    export default {
        name: "PlayList",
        components: {
            SongComp
        },
        props: {
            songs: {
                type: Array
            }
        }
    }
</script>

<style scoped>

</style>