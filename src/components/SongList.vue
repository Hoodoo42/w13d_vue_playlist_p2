<template>
  <div>
    <h4 v-for="song in song_info" :key="song[`song_id`]" @click="create_playlist">{{song[`title`]}}
    </h4>
  </div>
</template>

<script>
export default {
    methods: {
        create_playlist() {
            this.$root.$emit(`playlist_created`, this.song_info)
        }
    },


  data() {
    return {
    song_info: [
        {
          title: `Imagine`,
          artist: `John Lennon`,
          song_id: `71`,
          img_url: `value`,
        },
        {
          title: `Ramble On`,
          artist: `Led Zeppelin`,
          song_id: `69`,
          img_url: `value`,
        },
        {
          title: `Santeria`,
          artist: `Sublime`,
          song_id: `96`,
          img_url: `value`,
        },
        {
          title: `Californication`,
          artist: `Red Hot Chilli Peppers`,
          song_id: `99`,
          img_url: `value`,
        },
        {
          title: `Riding for a fall`,
          artist: `Mad Caddies`,
          song_id: `07`,
          img_url: `value`,
        },
        {
          title: `Warmness on the soul`,
          artist: `Avenged 7x`,
          song_id: `01`,
          img_url: `value`,
        },
      ],
    };
  },
};
</script>

<style scoped>
</style>