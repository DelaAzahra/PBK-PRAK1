<template>
  <div>
    <h2>Daftar Hewan yang Dibooking</h2>
    <ul>
      <li v-for="(pet, index) in pets" :key="index">
        <strong :style="{ color: pet.type === 'Kucing' ? 'orange' : 'black' }">
          {{ pet.name }} ({{ pet.type }})
        </strong>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['pets']
}
</script>
