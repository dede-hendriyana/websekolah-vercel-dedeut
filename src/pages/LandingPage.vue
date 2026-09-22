<!-- <template>
  <div class="landingpage">
    <div class="belanja">
      <h1 class="judul1">Belanja Perlengkapan Olahraga Terlengkap</h1>
      <p class="judul2">Dari outfit,hingga alat olahraga--lengkap hanya disini</p>
      <RouterLink to="/product" class="button">Produk</RouterLink>
    </div>
    <video controls width="480" muted loop>
 <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
 Browser kamu tidak mendukung pemutaran video.
</video>

    <div class="Kategori">
      <div class="Posisikategori">
        <div class="kategori-card">
          <div class="kategori-icon">✅</div>
          <h3 class="kategori-judul">Kualitas Terbaik</h3>
          <p class="kategori-p">Bahan berkualitas tinggi untuk kenyamanan maksimal</p>
        </div>

        <div class="kategori-card">
          <div class="kategori-icon">💵</div>
          <h3 class="kategori-judul">Harga Terjangkau</h3>
          <p class="kategori-p">Harga yang kompetitif tanpa mengorbankan kualitas</p>
        </div>

        <div class="kategori-card">
          <div class="kategori-icon">🚚</div>
          <h3 class="kategori-judul">Gratis Ongkir</h3>
          <p class="kategori-p">Nikmati pengiriman gratis untuk semua pesanan di atas Rp100.000</p>
        </div>

      </div>
    </div>
  </div>
</template>

<script setup>

</script> -->
<template>
  <div class="landingpage">
    <div class="belanja">
      <h1 class="judul1">{{ judul }}</h1>

      <p class="judul2">{{ deskripsi }}</p>

      <RouterLink to="/product" class="button">
        {{ namaTombol }}
      </RouterLink>
    </div>

    <video autoplay controls width="480" muted loop>
      <source
        src="https://www.w3schools.com/html/mov_bbb.mp4"
        type="video/mp4"
      />
      Browser kamu tidak mendukung pemutaran video.
    </video>

    <div class="Kategori">
      <div class="Posisikategori">

        <KategoriCard
          icon="✅"
          judul="Kualitas Terbaik"
          deskripsi="Bahan berkualitas tinggi untuk kenyamanan maksimal"
        />

        <KategoriCard
          icon="💵"
          judul="Harga Terjangkau"
          deskripsi="Harga yang kompetitif tanpa mengorbankan kualitas"
        />

        <KategoriCard
          icon="🚚"
          judul="Cepat Sampai"
          deskripsi="Nikmati pengiriman gratis untuk semua pesanan di atas Rp100.000"
        />

      </div>
    </div>
  </div>
</template>

<script setup>
import KategoriCard from '../components/KategoriCard.vue'
defineProps({
  judul: {
    type: String,
    default: 'Belanja Perlengkapan Olahraga Terlengkap'
  },
  deskripsi: {
    type: String,
    default: 'Dari outfit hingga alat olahraga, lengkap hanya di sini.'
  },
  namaTombol: {
    type: String,
    default: 'Produk'
  }
})
</script>

<style scoped>

.landingpage {
  font-family: 'Poppins', sans-serif;
  color: #333333;
  margin-left: 20px;
}

.belanja {
  background: linear-gradient(135deg, #12c921, #377ef8);
  padding: 75px; 
  text-align: center;
  color: #ffffff;
  border-radius: 10px;
}

.judul1 {
  font-size: 2.5rem;
  margin-bottom: 15px;
}

.judul2 {
  font-size: 1.2rem;
  margin-bottom: 30px;
}

.button {
  background-color: #ffffff;
  color: #333333;
  font-weight: bold;
  padding: 12px 30px;
  border-radius: 25px;
}


.Kategori {
  padding: 60px;
  background-color: #fcfdfd;
}

.Posisikategori {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 60px; 
  max-width: 1200px;
}

.kategori-card {
  background-color: #8afff5;
  max-width: 300px;
  padding: 40px;
  text-align: center;
  border-radius: 12px; 
}
.kategori-card {
  box-shadow: 0 10px 25px black;
}

.kategori-icon {
  font-size: 30px;
  margin-bottom: 15px;
}

.kategori-judul {
  font-size: 30px;
  margin-bottom: 10px;
  color: #222222;
}

.kategori-p {
  font-size: 1rem;
  color: #666666;
}

video{
  margin-left: auto;
  margin-right: auto;
  margin-top: 50px;
  border-radius: 20px;
  display: block;
}
</style>