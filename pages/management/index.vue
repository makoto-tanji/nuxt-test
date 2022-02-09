<template>
  <div class="management">
    <h1>生徒管理ページ</h1>
    <table>
      <tr>
        <th>名前</th>
        <th>ID</th>
      </tr>
      <tr v-for="student in students" :key="student.id">
        <td>{{ student.name }}</td>
        <td>{{ student.id }}</td>
      </tr>
    </table>
    <NuxtLink to="/">戻る</NuxtLink>
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
.management {
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