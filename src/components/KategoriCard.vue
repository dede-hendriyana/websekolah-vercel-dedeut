<template>
  <div class="kategori-card">
    <div class="kategori-icon">{{ icon }}</div>
    <h3 class="kategori-judul">{{ judul }}</h3>
    <p class="kategori-p">{{ deskripsi }}</p>
  </div>
</template>

<script setup>
defineProps({
  icon: {
    type: String,
    required: true
  },
  judul: {
    type: String,
    required: true
  },
  deskripsi: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
.kategori-card {   
  width: 280px;
  min-height: 220px;
  padding: 25px;
  background-color: #ffffff;
  border-radius: 15px;
  text-align: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  box-sizing: border-box;
}


.kategori-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.kategori-icon {
  font-size: 45px;
  margin-bottom: 15px;
}

.kategori-judul {
  margin: 10px 0;
  color: #1e3a8a;
  font-size: 22px;
  font-weight: 700;
}

.kategori-p {
  margin: 0;
  color: #666666;
  font-size: 15px;
  line-height: 1.6;
}

/* Responsive untuk HP */
@media (max-width: 768px) {
  .kategori-card {
    width: 90%;
    max-width: 350px;
  }
}
</style>