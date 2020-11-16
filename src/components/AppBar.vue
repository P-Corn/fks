<template>
    <div>
        <v-toolbar
        color="cyan"
        dark
        fixed
        >
            
            <v-toolbar-title>Utensil Game</v-toolbar-title>

            <v-spacer></v-spacer>

            <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

        </v-toolbar>

        <!-- <v-tabs-items v-model="tab">
            <v-tab-item
                v-for="item in items"
                :key="item"
            >
            </v-tab-item>
        </v-tabs-items> -->

        <v-navigation-drawer
            v-model="drawer"
            absolute
            temporary
            bottom
        >
            <v-list
                nav
                dense
            >
                <v-list-item-group
                v-model="group"
                active-class="deep-purple--text text--accent-4"
                >
                <v-list-item class="nav-item">
                        <router-link color="green" class="nav-link" to="/">Home</router-link>
                </v-list-item>

                <v-list-item class="nav-item">
                        <router-link class="nav-link" to="/previousmatches">Previous matches</router-link>
                </v-list-item>

                <v-list-item class="nav-item">
                        <router-link class="nav-link" to="/submit">Sumbit score</router-link>
                </v-list-item> 
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </div>
</template>

<script>

export default {
  name: 'AppBar',
  components: {
      
  },
    data: () => ({
      drawer: false,
      group: null,
      tab: null,
        items: [
          'Submit', 'Current', 'History',
        ],
    }),

    watch: {
      group () {
        this.drawer = false
      },
    },
}
</script>

<style scoped lang="scss">

a {
    color:inherit;
    text-decoration: none;
}

.nav-item {
    text-align: center;
}

</style>