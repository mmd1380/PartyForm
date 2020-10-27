<template>
  <v-card style="position: fixed;">
    <v-navigation-drawer
      temporary
      right
      fixed
      dir="rtl"
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
  </v-card>
</template>

<script>
export default {
  data: () => ({
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