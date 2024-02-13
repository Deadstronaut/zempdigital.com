<template>
  <q-page>
    <!-- BLACK HEADER -->
    <q-header id="appHeader">
      <div id="headerToolbar">
        <q-toolbar class="text-white">
          <!-- Koşullu gösterim için showHeaderLogo computed property'sini kullan -->
          <q-img
            v-if="showHeaderLogo"
            class="headerLogo"
            src="src/assets/logosmall.png"
          />
          <q-img v-else class="headerLogo" src="src/assets/zemp.png" />
          <q-space />

          <q-btn id="btnTeam" flat style="color: #FF0080" label="Home" to="/" />
        </q-toolbar>
      </div>
    </q-header>
    <!-- END OF HEADER -->

      <!-- PAGE -->
      <div id="teamPage">
        <q-parallax
          src="src\assets\teambg.png"
          :width="1920"
          style="height: 880px; width: 100vw; height: 30vh"
        >
        </q-parallax>
        <!-- TEAM ABOUT PART -->
        <div class="teamContainer" style="">
          <div class="teamAboutPart row q-py-xl">
            <!-- Paragraph Left -->
            <div class="col justify-between">
              <div id="teamPara1" class="col-12 col-md-6">
                <p id="teamAbout" class="text-bold">About Zemp Consulting ;
                  <q-btn outline round color="black" icon="card_giftcard" />
                </p>

                <p>
                  Zemp Consulting offers the most inclusive design service, covering
                  start-to-end design needs and ensuring coherence with branding and
                  asset creation services. Our UI/UX services cater to app
                  development, web development, and custom touchpoint design. The
                  design process begins with targeted research tailored to your needs
                  and culminates in professional delivery.
                </p>

              </div>

              <!-- COLORFUL PART -->
              <div id="colorfulText" class="col q-py-lg row justify-start">
                <div class="text-bold q-mr-sm" style="font-size: 32px; color: #3ddeed">
                    Design
                  </div>
                  <div class="text-bold q-mr-sm" style="font-size: 32px; color: #71f285">
                  Development
                </div>
                <div class="text-bold q-mr-xs" style="font-size: 32px; color: #cb00dd">
                  Project Management
                </div>
              </div>

              <!-- Paragraph Right (Middle) -->
              <div id="teamPara2" class="aboutParts col-xl-5 col-lg-5 col-md-6 col-sm-12">
                <p>
                  Zemp Consulting offers the most inclusive design service, covering
                  start-to-end design needs and ensuring coherence with branding and
                  asset creation services. Our UI/UX services cater to app
                  development, web development, and custom touchpoint design. The
                  design process begins with targeted research tailored to your needs
                  and culminates in professional delivery.
                </p>
              </div>
            </div>
          </div>
        </div>

        <!-- TEAM CARD  -->
        <div class="teamCards col row q-pb-xl text-white justify-evenly">
              <!-- Patrick Zemp Card-->
              <div class="column items-center col-xl-4 col-lg-3 col-md-4 col-sm-5 col-xs-12">
                  <q-card class="my-card  q-my-md" flat bordered>
                    <q-card-section horizontal class="justify-between">
                      <q-card-section class="q-pt-md " >
                      <div class="text-h5 q-mt-sm q-mb-xs">Patrick Zemp</div>
                      <div class="text-caption">Founder/Manager</div>
                      <!-- <div class="text-overline text-grey" style="max-width: 22vw;">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        <q-separator />
                      </div> -->
                      <div class="q-pt-lg text-caption text-grey q-gutter-sm">
                        <q-btn size="11px" outline round color="white" icon="card_giftcard" />
                        <q-btn size="11px" outline round color="white" icon="card_giftcard" />
                      </div>

                    </q-card-section>


                    <q-img
                        class="teamPhoto"
                        src="src\assets\patrick.png"
                        />


                      </q-card-section>

                </q-card>
              </div>


              <!-- Goktug Dulger Card-->
              <div class="column items-center col-xl-4 col-lg-3 col-md-4 col-sm-5 col-xs-12">
                  <q-card class="my-card  q-my-md" flat bordered>
                    <q-card-section horizontal class="justify-between">
                      <q-card-section class="q-pt-md">
                      <div class="text-h5 q-mt-sm q-mb-xs">Göktuğ Dülger</div>
                      <div class="text-caption">Lead Developer</div>
                      <!-- <div class="text-overline text-grey" style="max-width: 22vw;">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        <q-separator />
                      </div> -->
                      <div class="q-pt-lg text-caption text-grey q-gutter-sm">
                        <q-btn size="11px" outline round color="white" icon="card_giftcard" />
                        <q-btn size="11px" outline round color="white" icon="card_giftcard" />
                      </div>

                    </q-card-section>


                    <q-img
                        class="teamPhoto"
                        src="src/assets/goktug.png"
                        />


                      </q-card-section>

                </q-card>
              </div>


              <!-- Irem Buyukcingil Card-->
              <div class="column items-center col-xl-4 col-lg-3 col-md-4 col-sm-5 col-xs-12">
                  <q-card class="my-card  q-my-md" flat bordered>
                    <q-card-section horizontal class="justify-between">
                      <q-card-section class="q-pt-md">
                      <div class="text-h5 q-mt-sm q-mb-xs">Irem Buyukcingil</div>
                      <div class="text-caption">Frontend Developer</div>
                      <!-- <div class="text-overline text-grey" style="max-width: 22vw;">
                        Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                        <q-separator />
                      </div> -->
                      <div class="q-pt-lg text-caption text-grey q-gutter-sm">
                        <q-btn size="11px" outline round color="white" icon="card_giftcard" />
                        <q-btn size="11px" outline round color="white" icon="card_giftcard" />
                      </div>

                    </q-card-section>


                    <q-img
                        class="teamPhoto"
                        src="src\assets\irem.png"
                        />


                      </q-card-section>

                </q-card>
              </div>

          </div>
            <!-- END OF TEAM CARDS -->
    </div>
    <!-- END OF PAGE -->



    <!-- Bottom Square -->
    <div
      class="q-mt-xl"
      style="width: 100%; position: absolute;"
    >
      <div class="" style="height: 40vh; background-color: #000">
        <div class="q-pa-lg">
          <q-img
            class="footerLogo q-ml-sm"
            src="src/assets/logosmall.png"
          />
        </div>
      </div>
    </div>
  </q-page>
</template>


<script setup>
import { ref, onMounted, onUnmounted, computed } from "vue";
// import { matMenu } from '@quasar/extras/material-icons'
// import { mdiAbTesting } from '@quasar/extras/mdi-v6'
// import { fasFont } from '@quasar/extras/fontawesome-v5'

const windowWidth = ref(window.innerWidth);

// Ekran boyutunu dinlemek için bir event listener oluştur
const updateWidth = () => {
  windowWidth.value = window.innerWidth;
};

onMounted(() => {
  window.addEventListener("resize", updateWidth);
});

onUnmounted(() => {
  window.removeEventListener("resize", updateWidth);
});

// Koşullu gösterim için computed property kullan
const showHeaderLogo = computed(() => windowWidth.value <= 767);


</script>
