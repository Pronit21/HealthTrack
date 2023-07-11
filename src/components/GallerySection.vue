<template>
    <v-container class="my-15 text-center">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
                <v-subheader class="text-h4" justify="center">
                    Gallery
                </v-subheader>
                <p>Explore our gallery of inspiring transformations and healthy lifestyle moments captured by our community.</p>

            </v-col>

            <v-col
      v-for="n in 9"
      :key="n"
      class="d-flex child-flex"
      cols="4"
    >
      <v-img
        :src="`https://source.unsplash.com/featured/?sports=${n * 5 + 10}`"
        :lazy-src="`https://source.unsplash.com/featured/?sports=${n * 5 + 10}`"
        aspect-ratio="1"
        class="grey lighten-2"
      >
        <template v-slot:placeholder>
          <v-row
            class="fill-height ma-0"
            align="center"
            justify="center"
          >
            <v-progress-circular
              indeterminate
              color="grey lighten-5"
            ></v-progress-circular>
          </v-row>
        </template>
      </v-img>
    </v-col>

        </v-row>
    </v-container>
</template>

<script>
    export default {
        name: "GallerySection"
    }

</script>

<style scoped>
.text-h4{
  font-weight: bold;
}

</style>