<template>
    <div>
        <li>
            <button @click="addSong"> {{ buttonLabel }} </button>
            <h2 class="title"> "{{ songMetaData.title }}" </h2>
            <h2 class="artist"> by: {{ songMetaData.artist }} </h2>
        </li>
    </div>
</template>

<script>
    export default {
        name: "SongComp",
        props: {
            songMetaData: {
                type: Object,
            },
            addSong: {
                type: Function,
            },
            buttonLabel:{
                type: String,
            }
        }
    }
</script>

<style scoped>

button {
    height: 5vh;
    padding: 1.5vh;
    margin-top: 1.8vh;
}

li {
    display: flex;
    flex-direction: row;
    padding: 0.5vw;
    height: 10vh;
}
h2 {
    padding-left: 2vw;
    width: 100%;
}
.artist {
    font-weight: normal;
}


</style>