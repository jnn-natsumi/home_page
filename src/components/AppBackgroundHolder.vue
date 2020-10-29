<template>
    <section class="background-holder">
        <v-container fluid fill-height class="background-holder__content">
            <v-row>
                <v-col class="background-holder__content-text">
                    <p><strong>{{ title  }}</strong></p>
                </v-col>
            </v-row>
        </v-container>
    </section>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.background-holder__content {
    background: url("../assets/img/background.jpg");
    background-size: cover;
    background-position: center center;
    width: 100%;
    height: 30vh;

    &-text {
        font-family: 'Staatliches', cursive;
        color: white;
        text-align: center;
        font-size: 28px;
        font-weight: bold;

        @include display_pc {
            font-size: 40px;
        }

    }
    strong {
        background: linear-gradient(transparent 50%, rgba(0, 0, 0, 0.6));
    }
}
</style>
