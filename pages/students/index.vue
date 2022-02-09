<template>
  <div class="students">
    <h1>生徒一覧</h1>
    <ul>
      <li v-for="(student, index) in students" :key="index">
        <NuxtLink :to="{name: 'students-id', params: {id: student.id}}">{{ student.name }}</NuxtLink>
      </li>
    </ul>
  </div>
</template>


<script>
export default {
  data() {
    return {
      students: [
        {
          id: "qnfungqxllc3m1ak",
          name: "生徒A",
        },
        {
          id: "7j9cumkgsq6l264c",
          name: "生徒B",
        },
        {
          id: "eo34bhey9m0d92ou",
          name: "生徒C",
        },
      ],
    };
  },
};
</script>


<style>
.students {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  /*  */
  flex-direction: column;
}
</style>