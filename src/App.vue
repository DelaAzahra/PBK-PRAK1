<template>
  <div id="app">
    <h1>🐾 Pet Hotel Booking</h1>
    <PetForm @add-pet="addPet" />
    <BookingStatus :pets="pets" />
    <PetList :pets="pets" />
  </div>
</template>

<script>
import PetForm from './components/PetForm.vue'
import PetList from './components/PetList.vue'
import BookingStatus from './components/BookingStatus.vue'

export default {
  components: { PetForm, PetList, BookingStatus },
  data() {
    return {
      pets: []
    }
  },
  methods: {
    addPet(pet) {
      this.pets.push(pet)
    }
  }
}
</script>
