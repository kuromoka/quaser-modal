<template>
  <q-page class="flex flex-center column">
    <q-btn label="Modal" color="primary" @click="modal = true" />

    <q-dialog v-model="modal">
      <q-card>
        <q-card-section>
          <div class="text-h6">Modal</div>
        </q-card-section>

        <q-card-section>
          <q-input v-model="text" label="Text" />
        </q-card-section>

        <q-card-actions align="right">
          <q-btn flat label="OK" color="primary" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
    <p>{{ text }}</p>
  </q-page>
</template>

<script>
export default {
  name: 'PageIndex',
  data () {
    return {
      modal: false,
      text: ''
    }
  }
}
</script>
