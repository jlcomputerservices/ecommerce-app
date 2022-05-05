<template>
  <div class="container">
    <div class="d-flex justify-content-center">
      <b-card
        v-for="data in dataList"
        :bg-variant="data.variant"
        text-variant="white"
        :header="data.name"
        class="text-center mx-3 mb-3"
        :key="data"
      >
        <b-card-text>{{ data.description }}</b-card-text>
      </b-card>
    </div>
    <template v-if="dataList.length > 4">
      <div class="d-flex justify-content-center">
        <b-pagination
          v-model="currentPage"
          pills
          :total-rows="rows"
          size="sm"
        />
      </div>
    </template>
  </div>
</template>

<script>
export default {
  name: "ProfileCards",
  data: () => ({
    dataList: [
      {
        id: 1,
        name: "Pitok",
        description: "Full Stack Developer",
        variant: "primary",
      },
      {
        id: 2,
        name: "Joan",
        description: "Quality Assurance",
        variant: "secondary",
      },
      {
        id: 3,
        name: "Lexie",
        description: "Software Engineer",
        variant: "success",
      },
      {
        id: 4,
        name: "Chester",
        description: "Frontend Developer",
        variant: "dark",
      },
      {
        id: 5,
        name: "Justin",
        description: "Frontend Developer",
        variant: "secondary",
      },
      {
        id: 6,
        name: "Joshua",
        description: "Frontend Developer",
        variant: "primary",
      },
    ],
    rows: 100,
    currentPage: 1,
  }),
};
</script>
