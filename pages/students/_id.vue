<template>
  <div class="student_id">
    <!-- <p>パラメータ：{{ $route.params.id }}</p> -->
    <h1>{{ student.name }}</h1>
    <div class="link">
      <NuxtLink to="/students">生徒一覧へ戻る</NuxtLink>
    |
    <NuxtLink to="/">トップぺージへ</NuxtLink>
    </div>
  </div>
</template>


<script>
export default {
  validate({ params }) {
    return /^\w+$/.test(params.id)
    // ^:行の先頭にマッチ
    // \:次の文字をエスケープ
    // \d:数字に一致。[0-9]と同義
    // \w:文字に一致
    // +:直前の文字の1文字以上の繰り返しにマッチ
    // $:行の末尾にマッチ
  },
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
      student: "",
    };
  },
  methods: {
    getStudent(){
      this.student = this.students.find( ({id}) => id === this.$route.params.id);
    }
  },
  created(){
    this.getStudent();
  }
};
</script>


<style>
.student_id {
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