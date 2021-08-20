<template>
    <div>
        <Song-List
        id="songlist"
        :songs="songs"
        v-on:addtoPlaylist="addtoPlaylist($event)"/>
        <Play-List
        id="playlist"
        :songs="playlist"
        v-on:addtoPlaylist="removefromPlaylist($event)"/>
        />
    </div>
</template>

<script>
import PlayList from './Play-List.vue'
import SongList from './Song-List.vue'
    export default {
        name: "PageBody",
        components: {
            SongList,
            PlayList,
        },
        data: () => {
            return {
                songs: [
                    {
                        title: "Shoulders",
                        artist: "Coheed and Cambria"
                    },
                    {
                        title: "How not to Drown",
                        artist: "CHVRCHES ft. Robert Smith"
                    },
                    {
                        title: "Bunny is a Rider",
                        artist: "Caroline Polachek"
                    },
                    {
                        title: "One Last Kiss",
                        artist: "Utada Hikaru"
                    },
                    {
                        title: "Medusa",
                        artist: "GRiZ, Wreckno"
                    },
                    {
                        title: "XS",
                        artist: "Rina Sawayama"
                    },
                    {
                        title: "Driver",
                        artist: "Pendulum"
                    },
                    {
                        title: "Kingslayer ft. BABYMETAL",
                        artist: "Bring me the Horizon"
                    },
                    {
                        title: "MAYDAY ft. Ryo",
                        artist: "coldrain"
                    },
                ],
                playlist: []
            }
        },
        methods: {
            addtoPlaylist(songIndex) {
                console.log(songIndex);
                this.playlist.push(this.songs[songIndex]);
                this.songs.splice(songIndex, 1);
            },
            removefromPlaylist(songIndex) {
                console.log(songIndex);
                this.songs.push(this.playlist[songIndex]);
                this.playlist.splice(songIndex, 1);
            }
        }
    }
</script>

<style scoped>

div {
    display: grid;
    grid-auto-columns: 1fr 1fr;
    grid-auto-rows: auto;
}
#songlist {
    display: grid;
    grid-column: 1/2;
    justify-self: left;
    width: 45vw;
        padding: 0.5vw;
    border: 3px solid #2F2F2F;
    border-radius: 16px;
}
#playlist {
    display: grid;
    grid-column: 2/3;
    justify-self: right;
    width: 45vw;
    padding: 0.5vw;
    border: 3px solid #2F2F2F;
    border-radius: 16px;
}

</style>