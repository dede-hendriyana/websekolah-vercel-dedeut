<script setup>
import { ref } from 'vue'
defineProps(['nama', 'harga', 'gambar'])
const gambarDipilih = ref(null)
function bukaPreview(src) {
 gambarDipilih.value = src
}
function tutupPreview() {
 gambarDipilih.value = null
}
</script>
<template>
 <div class="card">
 <img :src="gambar" :alt="nama" @click="bukaPreview(gambar)" />
 <h3>{{ nama }}</h3>
 <p>Rp {{ harga.toLocaleString('id-ID') }}</p>
<button class="button">Beli Sekarang</button>
 </div>
 <div v-if="gambarDipilih" class="preview-overlay">
    <button @click="tutupPreview">Tutup</button>
 <img :src="gambarDipilih" class="preview-besar" />
 </div>
</template>
<style scoped>
.card {
 border: 1px solid #ddd;
 border-radius: 10px;
 padding: 14px;
 width: 200px;
 text-align: center;
}
.button{
    padding: 10px 15px;
    background: rgb(200, 255, 0);
    color: rgb(241, 0, 0);
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
.card img { width: 100px; border-radius: 6px; cursor: pointer; height: 100px; }
.preview-overlay {
 position: fixed; top: 0; left: 0; width: 100%; height: 100%;
 background: rgba(0, 0, 0, 0.7);
 display: flex; align-items: center; justify-content: center;
 cursor: zoom-out;
}
.preview-besar { max-width: 80%; max-height: 80%; border-radius: 8px; }
</style>