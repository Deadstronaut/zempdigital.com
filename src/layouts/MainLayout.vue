<template>
  <q-layout view="lHh Lpr lFf">
        <!-- BLACK HEADER -->
        <!-- <q-header
          class="q-py-xs q-px-xl"
          style="height: 100px; background-color: #000000"
        >
          <div class="q-pa-lg">
            <q-toolbar class="text-white">
              <q-img
                src="src\assets\zemp.png"
                style="width: 160px; height: 36px"
              />
              <q-space />

              <q-tabs shrink no-caps>
                <q-tab
                  class="header-tabs"
                  name="frame1"
                  label="About"
                  @click="goToSection('frame1')"
                />
                <q-tab
                  class="header-tabs"
                  name="frame2"
                  label="Services"
                  @click="goToSection('frame2')"
                />
                <q-tab
                  class="header-tabs"
                  name="frame3"
                  label="Packages"
                  @click="goToSection('frame3')"
                />
                <q-tab
                  class="header-tabs"
                  name="frame4"
                  label="Contact"
                  @click="goToSection('frame4')"
                />

              </q-tabs>
            </q-toolbar>
          </div>
        </q-header> -->
        <!-- HEADER ENDS HERE -->



    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script setup>
// import {ref} from 'vue'

// const tab = ref('About')

</script>

<script>
// export default {
//   methods: {
//     goToSection(sectionId) {
//       // Belirtilen bölüme gitmek için JavaScript kullanarak scrollIntoView() metodunu kullanabilirsiniz.
//       const el = document.getElementById(sectionId);
//       if (el) {
//         el.scrollIntoView({ behavior: 'smooth', block: 'start' });
//       }
//     },
//   }
// }
</script>


<!-- aşağı yönlü tab scroll

    goToSection(sectionId) {
      // Belirtilen bölüme gitmek için JavaScript kullanarak scrollIntoView() metodunu kullanabilirsiniz.
      const el = document.getElementById(sectionId);
      if (el) {
        el.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    }


    yukarı yönlü tab scroll

goToSection(sectionId) {
  const el = document.getElementById(sectionId);
  if (el) {
    el.scrollIntoView({ behavior: 'smooth', block: 'start', inline: 'nearest' });
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }
} -->
