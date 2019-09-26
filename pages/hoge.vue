<template>
  <v-layout>
    <v-flex class="text-center">
    <v-stepper v-model="e1" vertical>
        <v-stepper-step editable step="1">
          hogehoge
        </v-stepper-step>
        <v-stepper-content step="1">
          <v-list >
            <v-subheader>
              TypeItems
            </v-subheader>
            <draggable v-model="items" :options="{group:'hoge'}" >
              <v-list-item key="1">
                <v-list-item-content>
                  <v-list-item-title >hogehoge</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
              <v-list-item key="2">
                <v-list-item-content>
                  <v-list-item-title >fugafuga</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </draggable>
          </v-list>
          <v-btn color="primary" @click="e1=2">Next</v-btn>
        </v-stepper-content>
    </v-stepper>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  data () {
    return {
      e1 : 0,
      items: [
        { key: "1", value: "人からよく思われている人柄" ,typeItems: [{ key: "1", value: "111A"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}], nextKey: "2", beforeKey: ""},
        { key: "2", value: "自覚がある自分の傾向" ,typeItems: [{ key: "1", value: "111"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}]},
        { key: "3", value: "人からよく思われていない所" ,typeItems: [{ key: "1", value: "111"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}]},
        { key: "4", value: "つい、やりがちな行動" ,typeItems: [{ key: "1", value: "111"},{ key: "2", value: "112"},{ key: "3", value: "113"},{ key: "4", value: "114"}]}
      ] 
    } 
  }
}
</script>

