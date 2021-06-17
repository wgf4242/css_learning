<template>
  <div class="home">
    <header>css 架构</header>

    <cmain>
      <article></article>
    </cmain>

    <cfooter></cfooter>
  </div>
</template>

<style lang="scss" scoped>
header {
  width: 200px;
  height: 200px;
  background-color: rgba($color: #000000, $alpha: 0.4);
  color: #fff;
  @include box-center(center, center);
};
</style>
