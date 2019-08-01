<template>
  <div>
    <Banner />
    <NewsInformation />
    <Publicity/>
    <SilhouettePicture/>
  </div>
</template>

<script>
import Banner from "./Main-content-template/Banner";
import NewsInformation from "./Main-content-template/News-information";
import Publicity from "./Main-content-template/Publicity"
import SilhouettePicture from "./Main-content-template/SilhouettePicture"
export default {
  components: {
    Banner,
    NewsInformation,
    Publicity,
    SilhouettePicture
  }
};
</script>

<style>
</style>
