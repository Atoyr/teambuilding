<template>
  <v-layout>
    <v-stepper v-model="e1" vertical>
      <template v-for="item in  items">
        <v-stepper-step editable v-bind:step="item.key">
          {{ item.value }}
        </v-stepper-step>
        <v-stepper-content v-bind:step="item.key">
          <v-list >
            <v-subheader>
              TypeItems
            </v-subheader>
            <draggable v-model="items" :options="{group:'{{ item.key }}'}" >
            <template v-for="typeItem in item.typeItems" >
              <v-list-item :key="typeItem.key">
                <v-list-item-content>
                  <v-list-item-title >{{ typeItem.value }}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </template>
            </draggable>
          </v-list>
          <v-btn v-if="item.prevKey  !== ''" outlined color="primary" @click="e1=(item.prevKey)">Prev</v-btn>
          <v-btn v-if="item.nextKey !== ''" color="primary" @click="e1=(item.nextKey)">Next</v-btn>
        </v-stepper-content>
      </template>
    </v-stepper>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  layout: "none",
  data () {
    return {
      e1 : 0,
      items: [
        { key: "1", value: "人からよく思われている人柄" ,typeItems: [{ key: "1", value: "111A"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}], nextKey: "2", prevKey: ""},
        { key: "2", value: "自覚がある自分の傾向" ,typeItems: [{ key: "1", value: "111"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}], nextKey: "3", prevKey: "1"},
        { key: "3", value: "人からよく思われていない所" ,typeItems: [{ key: "1", value: "111"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}], nextKey: "4", prevKey: "2"},
        { key: "4", value: "つい、やりがちな行動" ,typeItems: [{ key: "1", value: "111"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}], nextKey: "", prevKey: "3"}
      ] 
    } 
  }
}
</script>
