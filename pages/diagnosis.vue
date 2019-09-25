<template>
  <v-layout>
    <v-stepper v-model="e1" vertical>
      <v-stepper-step
        step="1">
        人からよく思われている人柄
      </v-stepper-step>
      <v-stepper-content step="1">
        hogehoge
        <v-btn color="primary" @click="e1=2">Next</v-btn>
      </v-stepper-content>
      <v-stepper-step
        step="2">
        自覚がある自分の傾向
      </v-stepper-step>
      <v-stepper-content step="2">
        fugufugu
      <v-btn color="normal" @click="e1=1">back</v-btn>
      <v-btn color="primary" @click="e1=3">Next</v-btn>
      </v-stepper-content>
      <v-stepper-step
        step="3">
        人からよく思われていない所
      </v-stepper-step>
      <v-stepper-content step="3">
        fugufugu
      <v-btn color="normal" @click="e1=2">back</v-btn>
      <v-btn color="primary" @click="e1=4">Next</v-btn>
      </v-stepper-content>
      <v-stepper-step
        step="4">
        つい、やりがちな行動
      </v-stepper-step>
      <v-stepper-content step="4">
        fugufugu
      <v-btn color="normal" @click="e1=3">back</v-btn>
      <v-btn color="primary" @click="e1=5">Next</v-btn>
      </v-stepper-content>
      <v-stepper-step
        step="5">
        よくあること
      </v-stepper-step>
      <v-stepper-content step="5">
        fugufugu
      <v-btn color="normal" @click="e1=4">back</v-btn>
      <v-btn color="primary" @click="e1=6">Next</v-btn>
      </v-stepper-content>
      <v-stepper-step
        step="6">
        コミュニケーションの特徴
      </v-stepper-step>
      <v-stepper-content step="6">
        fugufugu
      <v-btn color="normal" @click="e1=5">back</v-btn>
      <v-btn color="primary" @click="e1=7">Next</v-btn>
      </v-stepper-content>
      <v-stepper-step
        step="7">
        自分を象徴するワード
      </v-stepper-step>
      <v-stepper-content step="7">
        fugufugu
      <v-btn color="normal" @click="e1=6">back</v-btn>
      <v-btn color="primary" @click="e1=1">Next</v-btn>
      </v-stepper-content>
  </v-stepper>
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
      e1 : 0
    } 
  }
}
</script>
