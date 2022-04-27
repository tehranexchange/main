<template>
  <div>
    <v-menu offset-y :close-on-content-click="false" color="accent">
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="transparent"
          v-bind="attrs"
          v-on="on"
          tile
        >
          Dropdown
        </v-btn>
      </template>
      <v-card>
      <v-autocomplete
              v-model="friends"
              :disabled="isUpdating"
              :items="people"
              solo
              flat
              color="blue-grey lighten-2"
              label="Select"
              item-text="name"
              item-value="name"
            >
              <template v-slot:selection="data">
                <v-chip
                  v-bind="data.attrs"
                  :input-value="data.selected"
                >
                  <v-avatar left>
    <IconCrypto coinname="ETH" color="color" format="svg" />
                  </v-avatar>
                  {{ data.item.name }}
                </v-chip>
              </template>
              <template v-slot:item="data">
                <template v-if="typeof data.item !== 'object'">
                  <v-list-item-content v-text="data.item"></v-list-item-content>
                </template>
                <template v-else>
                  <v-list-item-avatar>
    <IconCrypto coinname="ETH" color="color" format="svg" />
                  </v-list-item-avatar>
                  <v-list-item-content>
                    <v-list-item-title v-html="data.item.name"></v-list-item-title>
                  </v-list-item-content>
                </template>
              </template>
            </v-autocomplete>
            </v-card>
    </v-menu>
  </div>
</template>
<script>
export default {
    name:'MarketSelect',
    data(){
        return{
               autoUpdate: true,
        friends: ['Sandra Adams', 'Britta Holt'],
        isUpdating: false,
        name: 'Midnight Crew',
        people: [
          { header: 'Group 1' },
          { name: 'Sandra Adams', group: 'Group 1', avatar: null },
          { name: 'Ali Connors', group: 'Group 1', avatar: null },
          { name: 'Trevor Hansen', group: 'Group 1', avatar: null },
          { name: 'Tucker Smith', group: 'Group 1', avatar: null },
          { divider: true },
          { header: 'Group 2' },
          { name: 'Britta Holt', group: 'Group 2', avatar: null },
          { name: 'Jane Smith ', group: 'Group 2', avatar: null },
          { name: 'John Smith', group: 'Group 2', avatar: null },
          { name: 'Sandra Williams', group: 'Group 2', avatar: null },
        ],
        }
    }
}
</script>