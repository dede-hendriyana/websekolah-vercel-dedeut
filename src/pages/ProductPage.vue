<script setup>
import ProductCard from '../components/ProductCard.vue'
const daftarProduk = [
 { id: 1, nama: 'Ayam Bangkok', harga: 75000, gambar:
'https://awsimages.detik.net.id/community/media/visual/2023/11/20/ayam-bangkok.png?w=650' },
 { id: 2, nama: 'Naga Hama', harga: 350000, gambar:
'https://i.pinimg.com/236x/ae/fc/fb/aefcfb94bef9a31adc6bc0781988f19a.jpg' },
 { id: 3, nama: 'Zapati', harga: 120000, gambar:
'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRtAw7XdVMZWrrIHtk8Nr--qojgYOOP740XMZ5DGwkD7jvIep4CkYqpGTQJ&s=10' },
{ id: 4, nama: 'tai sapi', harga: 12000, gambar:
'https://png.pngtree.com/thumb_back/fh260/background/20220507/pngtree-cow-dung-in-fields-shovel-smell-shit-photo-image_30292706.jpg'},
{ id: 4, nama: 'Ayam retbul', harga: 1200000000, gambar:
'../public/ayam.jpg'},
]
</script>
<template>
 <main>
 <h1>Produk Kami</h1>
 <div class="grid">
 <ProductCard
 v-for="produk in daftarProduk"
 :key="produk.id"
 :nama="produk.nama"
 :harga="produk.harga"
 :gambar="produk.gambar"
 />
 </div>
 </main>
</template>
<style scoped>
.grid {
 display: flex;
 gap: 10px;
 flex-wrap: wrap;
}
</style>