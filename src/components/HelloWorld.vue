<template>
  <div 
  :class="{ toggled: isToggled}"
  class="nav d-flex flex-column">
    <div class="d-flex flex-row justify-content-end pr-2">
      <button @click="toggleNav" class="burger" type="button">
        <fa-icon icon="bars"></fa-icon>
      </button>
    </div>
    <ul>
      <li class="active d-flex flex-row justify-content-between align-items-center">
        <span>Home</span><fa-icon icon="home"></fa-icon>
      </li>
      <li class="d-flex flex-row justify-content-between align-items-center">
        <span>Profile</span><fa-icon icon="user"></fa-icon>
      </li>
      <li class="d-flex flex-row justify-content-between align-items-center">
        <span>Setting</span><fa-icon icon="wrench"></fa-icon>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      isToggled: false,
    }
  },
  methods: {
    toggleNav: function() {
      this.isToggled = !this.isToggled
    }
  }
}
</script>