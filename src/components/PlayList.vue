<template>
    <div>
<h4 ref="playlist_container" @click="add_to_play">{{song[`title`]}}</h4>

    </div>
</template>

<script>
    export default {
        methods: {
            display_playlist(song_info) {
                this.$refs[`playlist_container`][`innerText`] = song_info
            }
        },
        mounted () {
            this.$root.$on(`playlist_created`, this.display_playlist);
        },
    }
</script>

<style scoped>

</style>