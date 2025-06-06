<template>
  <div class="ground">
    <Header />
    <Memo />
    <Footer />
  </div>
</template>

<script>
import Header from "./GroundHeader.vue";
import Footer from "./GroundFooter.vue";
import Memo from "./GroundMemo.vue";

export default {
  components: { Header, Footer, Memo },
};
</script>
