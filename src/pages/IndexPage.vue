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

          <q-btn id="btnTeam" flat style="color: #FF0080" label="Meet the Team" to="teamPage" />
        </q-toolbar>
      </div>
    </q-header>
    <!-- HEADER ENDS HERE -->

    <!-- PAGE -->
    <div class="">
      <div id="">

        <!-- ONE PAGE LONG PROJECT WITH 4 PAGES -->
        <!-- START OF THE PROJECT -->
        <q-page>
          <!-- Parallax image -->
          <q-parallax
            src="src/assets/horImg.jpg"
            :width="1920"
            style="height: 880px; width: 100vw; height: 30vh"
          >
            <h2
              id="cdsHead"
              class="text-bold text-white absolute-bottom"
              text-white
            >
              <p>Creative,Digital,Solutions</p>
            </h2>
          </q-parallax>

          <!-- FIRST FRAME -->
          <div id="frame1" class="topSection">
            <!-- HEADER COLORFUL IMAGE -->
            <!-- <q-img src="src\assets\picture.png" style="z-index: -1">
            <h2 style=" position: absolute; bottom: -30px; left: 60px; margin: 0 0 20px 20px; "
                class="text-bold text-white absolute-bottom"
                text-white
                >
                Creative,Digital,Solutions
            </h2>
        </q-img> -->

            <!-- ABOUT PART -->
            <div class="container" style="">
              <div class="aboutPart row q-py-xl">
                <!-- Paragraph Left -->
                <div class="row justify-between">
                  <div
                    id="apPara1"
                    class="col-xl-5 col-lg-4 col-md-5 col-sm-12"
                  >
                    <p id="apAbout" class="text-bold">About</p>
                    <p>
                      Zemp Consulting offers the most inclusive design service,
                      covering start-to-end design needs and ensuring coherence
                      with branding and asset creation services. Our UI/UX
                      services cater to app development, web development, and
                      custom touchpoint design. The design process begins with
                      targeted research tailored to your needs and culminates in
                      professional delivery.
                    </p>

                  </div>

                  <!-- Paragraph Right (Middle) -->
                  <div
                    id="apPara2"
                    class="aboutParts col-xl-6 col-lg-4 col-md-6 col-sm-12"
                  >
                    <p>
                      Our full scope encompasses research, planning, UX
                      documentation, branding, prototyping, revisions, and
                      delivery preparation. We prioritize a
                      <span class="bold">pixel-perfect</span> mindset and
                      <span class="bold"
                        >specialize in responsive, cross-platform design
                      </span>
                      that meets <span class="bold">global standards.</span> Our
                      full scope encompasses research, planning, UX
                      documentation, branding, prototyping, revisions, and
                      delivery preparation. We prioritize a
                      <span class="bold">pixel-perfect </span> mindset and
                      <span class="bold"
                        >specialize in responsive, cross-platform design
                      </span>
                      that meets <span class="bold">global standards.</span>
                    </p>
                  </div>

                  <!-- Zemp Logo -->
                  <div id="apLogo" class="col-xl-4 col-lg-2 col-md-3 col-sm-12">
                    <img
                      src="src\assets\explorelogo.png"
                      style="height: 12em; max-width: 22em"
                    />
                  </div>
                </div>
              </div>
            </div>
          </div>
          <!-- END OF FIRST FRAME-->

          <!-- SECOND FRAME -->
          <div id="frame2" class="sections q-pl-md" style="background-color: #71f285">
            <div id="greenBox">
              <div class="section">
                <h3 class="spHeading q-pl-md">Services</h3>

                <q-list dense style="max-width: 95vw">
                  <!-- UI/UX Design -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('uiuxDesign')"
                  >
                    <q-item-section>UI/UX Design</q-item-section>
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.uiuxDesign
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <!-- class="hidden" verince çalışıyor -->
                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.uiuxDesign"
                    >
                      Zemp Consulting offers the most inclusive design service,
                      covering start-to-end design needs and ensuring coherence
                      with branding and asset creation services. Our UI/UX
                      services cater to app development, web development, and
                      custom touchpoint design. The design process begins with
                      targeted research tailored to your needs and culminates in
                      professional delivery, including asset libraries, Figma UI
                      documentation, and, if required, design guidelines. The
                      scope is flexible and designed according to your demands.
                      Our full scope encompasses research, planning, UX
                      documentation, branding, prototyping, revisions, and
                      delivery preparation. We prioritize a pixel-perfect
                      mindset and specialize in responsive, cross-platform
                      design that meets global standards.
                    </div>
                  </transition>

                  <!-- Branding Design -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('brandingDesign')"
                  >
                    <q-item-section>Branding Design</q-item-section>
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.brandingDesign
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>
                  <!-- class="hidden" verince çalışıyor -->
                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.brandingDesign"
                    >
                      <div class="fade-in-out" :class="{ show: isVisible }">
                        Branding Design is crucial for increasing market share
                        and competing on a global scale. This service helps
                        visualize your company's story, ensuring unique and
                        trendy designs. We recommend availing this service
                        approximately every five years to stay abreast of design
                        trends. If you aim to be a pioneer in your sector,
                        Branding Design is tailored for you. Beyond harmonizing
                        touchpoints like logos, transactional language, brand
                        colors, emails, and visual assets, it's imperative to
                        have branding documentation. This ensures your branding
                        can seamlessly evolve along with your company's growth.
                      </div>
                    </div>
                  </transition>
                  <!-- Custom Touchpoint Design -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('customTouchpointDesign')"
                  >
                    <q-item-section>Custom Touchpoint Design</q-item-section>
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.customTouchpointDesign
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.customTouchpointDesign"
                    >
                      Many companies have unique design needs based on their
                      products and services. Zemp Consulting provides custom
                      design services precisely for these demands. Every asset
                      can be tailor-made to suit your specific needs. This
                      strategy-heavy design service encompasses any type of
                      asset and onsite applications. We recommend scheduling a
                      consultation with our design experts to brainstorm and
                      pinpoint designs that can significantly enhance your
                      competitive edge.
                    </div>
                  </transition>
                  <!-- Mobile and Web Development -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('mobileWebDevelopment')"
                  >
                    <q-item-section>Mobile and Web Development</q-item-section>
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.mobileWebDevelopment
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.mobileWebDevelopment"
                    >
                      At the core of our mobile and web development lies our
                      adept use of Vue.js and Quasar. These frameworks allow us
                      to craft applications that transcend functionality—built
                      to be resilient, efficient, and future-ready. Thanks to
                      this technology, businesses enjoy applications operating
                      persistently at peak performance, requiring minimal
                      oversight. Whether it's the seamless crossplatform
                      performance or scalability without hindrance, Vue.js and
                      Quasar ensure your digital presence remains robust,
                      reliable, and ahead of the curve.
                    </div>
                  </transition>
                  <!-- Integrated Services for Digital Success -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('integratedServices')"
                  >
                    <q-item-section
                      >Integrated Services for Digital Success</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.integratedServices
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>
                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.integratedServices"
                    >
                      At our core, we are more than just a tech company; we are
                      architects of digital success. Our integrated services
                      encompass not only robust technological solutions but also
                      transformative design and branding expertise. Through our
                      comprehensive offerings, from crafting a captivating brand
                      identity to delivering fully operational web and mobile
                      applications, we equip businesses to conquer the digital
                      landscape with confidence. By seamlessly combining
                      technology and design, we empower companies to establish a
                      commanding presence in the digital market, driving success
                      and growth.
                    </div>
                  </transition>
                  <!-- Independent Database & Backend Services -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('databaseBackendServices')"
                  >
                    <q-item-section
                      >Independent Database & Backend Services</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.databaseBackendServices
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>
                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.databaseBackendServices"
                    >
                      Leveraging the power of Vue.js and Quasar empowers us to
                      architect systems that thrive with minimal intervention.
                      Beyond their functionalities, these frameworks
                      significantly reduce the personnel required for system
                      upkeep without compromising performance. Our
                      client-centric approach ensures your database remains
                      entirely under your control, showcasing our commitment to
                      empowering your digital endeavors. With our adept team
                      managing the backend, your systems continue to function
                      flawlessly while experiencing seamless updates and
                      maintenance.
                    </div>
                  </transition>
                  <!-- Tech Stack Overview -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('techStackOverview')"
                  >
                    <q-item-section>Tech Stack Overview</q-item-section>
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.techStackOverview
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.techStackOverview"
                    >
                      Through strategic integration of Vue.js and Quasar within
                      our technological framework, we drive not just innovation
                      but also a pragmatic approach to cost-efficiency. These
                      frameworks act as more than tools; they are a testament to
                      our commitment to streamlining maintenance and optimizing
                      operations. Seamlessly interwoven into our systems, Vue.js
                      and Quasar significantly reduce maintenance costs,
                      ensuring judicious allocation of resources for our
                      clients. The uninterrupted flow of operations during
                      updates is a hallmark of our technological prowess,
                      empowering businesses to maintain their momentum without
                      downtime. While our adept team works behind the scenes,
                      clients retain full control over their databases,
                      underscoring our dedication to seamless updates and
                      optimal performance. Our utilization of Vue.js and Quasar
                      isn't merely about cutting-edge innovation; it's about
                      creating a technology ecosystem that champions efficiency,
                      reliability, and client empowerment.
                    </div>
                  </transition>
                  <!-- IT Support & Services -->
                  <q-item
                    class="services"
                    clickable
                    v-ripple
                    @click="toggleContent('itSupportServices')"
                  >
                    <q-item-section>IT Support & Services</q-item-section>
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.itSupportServices
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.itSupportServices"
                    >
                      Our comprehensive IT support services go beyond
                      traditional offerings, ensuring your digital assets remain
                      optimized and efficient. Acting as your dedicated virtual
                      tech team, we provide proactive maintenance and
                      troubleshooting, guaranteeing the seamless operation of
                      your business. Trust us for reliable and professional IT
                      support that keeps your business running smoothly,
                      ensuring your technology remains an asset, not a concern.
                    </div>
                  </transition>
                </q-list>
              </div>
            </div>
          </div>
          <!-- END OF SECOND FRAME -->

          <!-- THIRD FRAME -->
          <div id="frame3" class="sections q-pl-md" style="background-color: #3ddeed">
            <div id="blueBox">
              <div class="section">
                <h3 class="spHeading q-pl-md">Packages</h3>
                <q-list dense style="max-width: 95vw">
                  <!-- Brand Identity Fusion (Branding + UI/UX) -->
                  <q-item
                    class="packages"
                    clickable
                    v-ripple
                    @click="toggleContent('brandIdentity')"
                  >
                    <q-item-section
                      >Brand Identity Fusion (Branding + UI/UX)</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.brandIdentity
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <!-- class="hidden" verince çalışıyor -->
                    <div
                      class="spContent"
                      v-show="contentVisibility.brandIdentity"
                    >
                      At Zemp Consulting, we fuse the art of branding with
                      intuitive user experiences. Our comprehensive approach
                      merges branding strategy seamlessly into UI/UX design,
                      ensuring a unified identity across digital touchpoints.
                      From crafting compelling brand stories to creating
                      user-centric designs, we synchronize every element to
                      resonate with your audience and enhance market presence.
                    </div>
                  </transition>
                  <!-- Interactive Development Solutions (UI/UX + Development) -->
                  <q-item
                    class="packages"
                    clickable
                    v-ripple
                    @click="toggleContent('interactiveDevelopment')"
                  >
                    <q-item-section
                      >Interactive Development Solutions (UI/UX +
                      Development)</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.interactiveDevelopment
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.interactiveDevelopment"
                    >
                      Our expertise extends beyond design into the realm of
                      development. Seamlessly integrating UI/UX principles, we
                      develop responsive and captivating web and mobile
                      applications. Our approach unifies user-centric design
                      with robust technological solutions, crafting digital
                      experiences that are not just visually appealing but also
                      functionally efficient and future-ready.
                    </div>
                  </transition>
                  <!-- Tailored Touch-points (C. Touchpoint + Integrated Services) -->
                  <q-item
                    class="packages"
                    clickable
                    v-ripple
                    @click="toggleContent('tailoredTouchpoints')"
                  >
                    <q-item-section
                      >Tailored Touch-points (C. Touchpoint + Integrated
                      Services)</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.tailoredTouchpoints
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.tailoredTouchpoints"
                    >
                      For unique design needs, we provide tailored solutions.
                      Our custom design services cater to diverse demands,
                      precisely crafting assets and on-site applications that
                      elevate your competitive edge. Collaborate with our design
                      experts to conceptualize and implement designs that
                      distinctly represent your brand, bolstering your market
                      positioning.
                    </div>
                  </transition>

                  <!-- Mobile & Web Excellence (Mobile & Web Dev. + UI/UX) -->
                  <q-item
                    class="packages"
                    clickable
                    v-ripple
                    @click="toggleContent('mobileWebExcellence')"
                  >
                    <q-item-section
                      >Mobile & Web Excellence (Mobile & Web Dev. +
                      UI/UX)</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.mobileWebExcellence
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.mobileWebExcellence"
                    >
                      In the realm of mobile and web development, our focus
                      remains on the fusion of design and functionality. With
                      expertise in UI/UX and adept use of technologies like
                      Vue.js and Quasar, we engineer applications that transcend
                      mere utility. These applications boast resilience,
                      efficiency, and seamless cross-platform performance,
                      ensuring a robust digital presence.
                    </div>
                  </transition>

                  <!-- Branding Strategies & Evolution (Branding + IT Support) -->
                  <q-item
                    class="packages"
                    clickable
                    v-ripple
                    @click="toggleContent('brandingStrategies')"
                  >
                    <q-item-section
                      >Branding Strategies & Evolution (Branding + IT
                      Support)</q-item-section
                    >
                    <q-space />
                    <q-icon
                      :name="
                        contentVisibility.brandingStrategies
                          ? 'bi-dash-circle-dotted'
                          : 'bi-plus-circle'
                      "
                    />
                  </q-item>

                  <transition name="fade">
                    <div
                      class="spContent"
                      v-show="contentVisibility.brandingStrategies"
                    >
                      We specialize in crafting and evolving brand identities
                      that stand the test of time. Empowering businesses to
                      thrive in the competitive digital landscape, we equip you
                      with a captivating brand identity and functional digital
                      assets. To take a stand on sector with this service we
                      follow sectoral trends, competitors and create periodic
                      design trends report. Keeping your branding edge updated,
                      combined with long term implementation support.
                    </div>
                  </transition>
                  <!-- END OF CONTENTS -->
                </q-list>
              </div>
            </div>
          </div>
          <!-- END OF THIRD FRAME -->

          <!-- FORTH FRAME -->
          <div id="frame4" class="bottomSection" style="background-color: white">
            <div class="threeBtnBox">
              <!-- This row will center the items -->
              <div class="row justify-evenly q-px-xs">
                <div class="col-xl-4 col-lg-4 col-md-4 col-sm-12">
                  <q-btn
                    class="threeBtn q-pa-md q-px-xl"
                    color="black"
                    label="Call"
                  >
                    <q-space />
                    <q-icon
                      class="threeIcon"
                      name="bi-telephone"
                      color="white"
                    />
                  </q-btn>
                </div>
                <div class="col-xl-4 col-lg-4 col-md-4 col-sm-12">
                  <q-btn
                    class="threeBtn q-pa-md q-px-xl"
                    color="black"
                    label="Mail"
                  >
                    <q-space />
                    <q-icon
                      class="threeIcon"
                      name="bi-envelope-open"
                      color="white"
                    />
                  </q-btn>
                </div>
                <div class="col-xl-4 col-lg-4 col-md-4 col-sm-12">
                  <q-btn
                    class="threeBtn q-pa-md q-px-xl"
                    color="black"
                    label="Reach"
                  >
                    <q-space />
                    <q-icon class="threeIcon" name="bi-geo-alt" color="white" />
                  </q-btn>
                </div>
              </div>
            </div>

            <!-- Bottom Square -->
            <div
              class="q-mt-xl"
              style="width: 100%; position: absolute; bottom: 0"
            >
              <div class="" style="height: 40vh; background-color: #000">
                <div class="q-pa-lg">
                  <q-img
                    class="footerLogo"
                    src="src/assets/logosmall.png"

                  />
                </div>
              </div>
            </div>
          </div>
          <!-- END OF FORTH FRAME -->
        </q-page>
        <!-- END OF PAGE -->
      </div>
    </div>
    <!-- END OF THE PAGE -->
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


const contentVisibility = ref({
  uiuxDesign: false,
  brandingDesign: false,
  customTouchpointDesign: false,
  mobileWebDevelopment: false,
  integratedServices: false,
  databaseBackendServices: false,
  techStackOverview: false,
  itSupportServices: false,
  // 2ND FRAME REFS
  brandIdentity: false,
  interactiveDevelopment: false,
  tailoredTouchpoints: false,
  mobileWebExcellence: false,
  brandingStrategies: false,
});

const toggleContent = (contentName) => {
  for (const key in contentVisibility.value) {
    if (key === contentName) {
      contentVisibility.value[key] = !contentVisibility.value[key];
    } else {
      contentVisibility.value[key] = false;
    }
  }
};
</script>
