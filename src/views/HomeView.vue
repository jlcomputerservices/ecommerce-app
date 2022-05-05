<template>
  <div class="home">
    <ProfileCards />
  </div>
</template>

<script>
// @ is an alias to /src
import ProfileCards from "@/components/ProfileCards.vue";

export default {
  name: "HomeView",
  components: {
    ProfileCards,
  },
};
</script>
