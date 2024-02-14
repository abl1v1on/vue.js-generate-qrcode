<script>
  import QrcodeVue from 'qrcode.vue';

  export default {
    components: {
      QrcodeVue
    },

    data() {
      return {
        value: '',
        size: 300
      }
    },


  }
</script>

<template>
  <div class="content">
    <h2 class="white-text mb-3">Введите ссылку</h2>
    <input v-model="value" type="text" class="form-control link-input mb-3" placeholder="Link">
    <qrcode-vue v-if="value.length > 1" :value="value" :size="size" level="H"></qrcode-vue>
  </div>
</template>

<style scoped>
.white-text {
  color: white;
}

.content {
  margin: 0 auto;
  margin-top: 300px;
  max-width: 300px;
  text-align: center;
}
</style>
