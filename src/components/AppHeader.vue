<template>
  <v-app-bar dir="rtl" class="text-h3" style="z-index: 999;" flat dense fixed>
    <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
    <v-spacer></v-spacer>
    <v-toolbar-title>فرم ثبت نام</v-toolbar-title>
    <!-- <v-card>
      <v-navigation-drawer
        temporary
        right
        fixed
        v-model="drawer"
      >
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>John Leider</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list nav>
          <v-list-item
            v-for="item in items"
            :key="item.title"
            link
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
    </v-card> -->
  </v-app-bar>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    items: [
      { title: 'خانه', icon: 'mdi-view-dashboard' },
      { title: 'درباره ما', icon: 'mdi-forum' },
      { title: 'تماس', icon: 'mdi-phone' },
      { title: 'پنل کاربری', icon: 'mdi-book' },
      { title: 'خروج', icon: 'mdi-door' },
    ] 
  })
}
</script>