<template>
  <div class="memo">
    <div class="act">
      <button class="btn btn-primary" @click="add()">+ 추가</button>
    </div>
    <ul>
      <li v-for="(item, index) in state.data" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
import { reactive } from "vue";

export default {
  setup() {
    const state = reactive({
      data: ["메모 1 내용", "메모 2 내용", "메모 3 내용", "메모 4 내용"],
    });

    const add = () => {
      state.data.push("추가된 메모 내용");
    };

    return { state, add };
  },
};
</script>

<style lang="scss" scoped>
.memo {
  .act {
    padding: 10px 10 5px 0;
    text-align: right;
  }

  ul {
    border-top: 1px solid #eee;
    list-style: none;
    padding: 15px;
    margin: 0;

    li {
      padding: 5px 10px;
      margin: 5px;
    }
  }
}
</style>
