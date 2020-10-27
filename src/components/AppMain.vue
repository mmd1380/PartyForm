<template>
  <v-card flat class="mt-12">
    <v-row no-gutters>
      <v-col cols="2" class="nav-links">
        <v-card flat style="position: fixed;" tile>
          <v-list shaped>
            <v-list-item-group
              color="primary"
            >
              <v-list-item
                v-for="(item, i) in items"
                :key="i"
                color="primary"
                :to="'#' + item.link"
                :id="item.link"
                style="min-width: 220px;"
              >
                <v-list-item-icon>
                  <v-icon v-text="item.icon"></v-icon>
                </v-list-item-icon>
                <v-list-item-content>
                  <v-list-item-title v-text="item.text"></v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-list-item-group>
          </v-list>
        </v-card>
      </v-col>
      <v-col cols="10" class="px-4 py-2" dir="rtl">
          <v-card flat v-for="item in items" :id="item.link" :key="item.text" dir="rtl" tile class="elevation-0" :ref="item.link">
            <a :name="item.text" :id="item.link">
              <v-card-text>
                <AppForm :section="item.link"/>
              </v-card-text>
            </a>
          </v-card>
      </v-col>      
    </v-row>
  </v-card>
</template>

<script>
import AppForm from "./Accordion/AppForm";

export default {
  components: { AppForm },
  data: () => ({
    items: [
      { text: 'مشخصات اصلی', icon: 'mdi-account', link: 'main' },
      { text: 'مشخصات تکمیلی', icon: 'mdi-check', link: 'complement' },
      { text: 'اطلاعات تماس ها', icon: 'mdi-phone', link: 'communicate' },
      { text: 'اطلاعات آدرس ها', icon: 'mdi-mail', link: 'address' },
    ],
  }),
  created() {
    console.log(this)
    this.$router.currentRoute.hash !== "#main" && this.$router.push("#main");
    // window.addEventListener("scroll", function(e) {
    //   const section = e.path[0].anchors;
    //   console.log(e)
    //   e.preventDefault();
    //   section.forEach((el, index) => {
    //     const offsets = el.getBoundingClientRect();
    //     if(offsets.top < 30 && offsets.height * (index + 1) > window.scrollY) {
    //       //if(offsets.top <= window.scrollY && offsets.top + offsets.height > window.scrollY){
    //       const links = document.querySelectorAll(".v-list-item.v-list-item--link");
    //       links.forEach(item => {
    //         item.classList.remove("v-list-item--active");
    //         if(item.innerText == el.name ) {
    //           console.log(el, item)
    //           item.classList.add("v-list-item--active");
    //           this.$router.push(`#${item.id}`)
    //         }
    //       });
    //     }
    //   });
    // }.bind(this));
  }
}
</script>

<style scoped>
.nav-links {
  min-height: 93vh !important;
  border-right: solid 1.5px #333;
  z-index: 99;
}
</style>
