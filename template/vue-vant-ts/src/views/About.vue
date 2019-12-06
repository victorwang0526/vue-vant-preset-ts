<template>
  <div class="about">
    <van-nav-bar
            title="关于"
            left-text="返回"
            right-text="新增"
            left-arrow
            @click-left="onClickLeft"
            @click-right="onClickRight"
    />
    <h1>This is an about page</h1>
  </div>
</template>

<script lang="ts">

  import {Component, Vue} from "vue-property-decorator";
  import {Toast} from "vant";

  @Component({
    name: 'about',
  })
  export default class extends Vue {
    onClickLeft() {
      this.$router.back();
    }
    onClickRight() {
      Toast('新增');
    }

  }
</script>