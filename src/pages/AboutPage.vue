<template>
    <div class="about-page">
        <!--bagian 1: cerita kami-->
        <section class="cerita-kami">
            <h1>cerita kami</h1>
            <div class="cerita-content">
                <div class="cerita-teks">
                    <p>
                        Kami adalah tim yang berdedikasi untuk memberikan pengalaman belanja terbaik bagi pelanggan kami. 
                        Dengan fokus pada kualitas produk, harga yang kompetitif, dan layanan pelanggan yang luar biasa, 
                        kami berkomitmen untuk memenuhi kebutuhan dan harapan Anda.
                    </p>
                    <P> PERJALANAN KAMI DI MULAI DARI KECINTAAN PADA HEINDAHAN ALAM DAN KEINGINAN UNTUK MELINDUNGI LINGKUNGAN. KAMI BERUSAHA UNTUK MENYEDIAKAN PRODUK YANG RAMAH LINGKUNGAN DAN BERKUALITAS TINGGI, SEHINGGA ANDA DAPAT BELANJA DENGAN TENANG DAN BERTANGGUNG JAWAB. </P>
                    <P> 
                        VISI KAMI ADALAH MENJADI PILIHAN UTAMA PELANGGAN UNTUK BELANJA ONLINE, DENGAN MENAWARKAN PRODUK YANG INOVATIF, BERKUALITAS, DAN TERJANGKAU. KAMI BERUSAHA UNTUK TERUS BERINOVASI DAN MENINGKATKAN LAYANAN KAMI UNTUK MEMENUHI HARAPAN PELANGGAN.
                    </P>
                </div>       
         <div class="cerita-gambar">
            <!-- ganti src dengan gambar asli jika tersedia -->
             <div class="gambar-container">
                <img src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgYLn9Q6rIxH837HSR3AcjPPis74BIQo1gz1pOVk2LCiWvBsf49MfGV_a-VG3fBlcNWm1zGfMw-L6qb7pIge2fqCAHaGh9n0gP0qczq12ASRMLt0XSe9FO2KnwlknmxEY1XkScILBEbZFhZVQIbCCBn8l67pejhm3ae73Le4rQHJiNoYcX1a-dXJ5SDWUmG/s1024/file_000000005348620a9cc0a8a34549e023.png" alt="Cerita Kami" />
           </div>
         </div>
         
         </div>
        </section>
        </div>
 <!-- bagian 2: tim kami -->
 <section class="tim-kami">
 <h1> tim kami </h1>
 <div class="tim-grid">
 <Teamcard
 v-for="anggota in daftartim"
    :key="anggota.id"
    :nama="anggota.nama"
    :jabatan="anggota.jabatan"
/>
</div>
    </section>
</template>
     
<script setup>
import KategoriCard from '../components/KategoriCard.vue'

const daftartim = [
  { id: 1, nama: 'John Doe', jabatan: 'CEO' },
  { id: 2, nama: 'Jane Smith', jabatan: 'CTO' },
  { id: 3, nama: 'Mike Johnson', jabatan: 'CFO' },
  { id: 4, nama: 'Emily Davis', jabatan: 'COO' }
]
 </script>
 <style scopen>
img {
    height: 100%;
    width: 100%;
    border-radius: 15px;
} 
.about-page {
   max-width: 1200px;
   margin: 0 auto;
   padding: 40px 20px ;
}
/* Bagian 1: Cerita Kami */
.cerita-kami h1{
    margin-bottom: 24px;
    color:rgb(224, 215, 250);
} 
.cerita-content {
    display: flex;
    align-items: center;
    gap: 40px;
}
.cerita-teks {
    flex: 1;
}
.cerita-teks p {
    line-height: 1.7;
    margin-bottom: 12px;
}
.cerita-gambar {
    flex: 1;
}
.placeholder-img {
    width: 100%;
    height: 280px;
    background-color: #f0f0f0;
    border-radius: 12px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-size: 3rem;
    color: #888888;
 }
 
 .placeholder-img span {
    font-size: 1.2rem;
    margin-top: 8px;
    
}
 
/* === tim kami === */
.tim-kami {
    margin-top: 60px;    
}
.tim-kami h1 {
    margin-bottom: 24px;
    color: antiquewhite;
} 
.tim-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 20px;
}

</style>

 
 
 

 
 
 
 
 
 
 
 
 