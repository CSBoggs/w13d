<template>
    <div>
        <h1>Music Library:</h1>
        <ol>
            <SongComp
                v-for="(song, index) in songs"
                :key="song.title"
                :buttonLabel="'Add'"
                :songMetaData="song"
                :addSong="() => $emit('addtoPlaylist', index)"
                />
        </ol>
    </div>
</template>

<script>
import SongComp from './Song-Comp.vue'
    export default {
        name: "SongList",
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