<template>
    <div>
<h4 ref="playlist_container" v-for="song in song_info" :key="song[`song_id`]"></h4>

    </div>
</template>

<script>
    export default {
        methods: {
            display_playlist(song_info) {
                this.$refs[`playlist_container`][`innerText`] = song_info[`title`]
            }
        },
        mounted () {
            this.$root.$on(`playlist_created`, this.display_playlist);
        },
    }
</script>

<style scoped>

</style>