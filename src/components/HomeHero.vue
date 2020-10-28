
<template>
    <section class="home-hero">
        <v-container fluid fill-height class="home-hero__content">
            <v-row>
                <v-col class="home-hero__content-text">
                    <p><strong>Welcome to  my website!</strong></p>
                    <p><strong>I'm aiming for an engineer.</strong></p>
                </v-col>
            </v-row>
        </v-container>
    </section>
</template>

<style lang="scss" scoped>
.home-hero__content {
    background: url("../assets/img/universal.jpg");
    background-size: cover;
    background-position: center center;
    width: 100%;
    height:  50vh;
    position: relative;

    @include display_pc {
    height: 100vh;
    }

    &-text {
        font-family: 'Londrina Outline', cursive;
        color: white;
        text-align: center;
        font-size: 28px;
        font-weight: bold;

        @include display_pc {
        font-size: 50px;
        }
    }
    strong {
        background: linear-gradient(transparent 30%, rgba(0, 0, 0, 0.4));
        }
}

.home-hero__content::before {
  content:"";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 0;
  border-style: solid;
  /*ここで三角形のサイズを決める。
  必ず幅100vwにして、ブラウザサイズいっぱいにしてください。*/
  border-width: 0 0 300px 100vw ;
  border-color: transparent transparent #fff transparent;
}
</style>
