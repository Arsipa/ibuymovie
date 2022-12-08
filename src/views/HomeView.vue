<template>
    <div class="home">
        <!-- <video loop autoplay muted poster="@/assets/video/mainVideoPreview.png">
          <source src="@/assets/video/back.mp4" type="video/mp4" />
          <source src="@/assets/video/back.webm" type="video/webm" />
        </video> -->
        <HelloWorld msg="Welcome to Your Vue.js App" />
    </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
    name: "HomeView",
    components: {
        HelloWorld,
    },
};
</script>

<style scoped>
video {
    width: 100%;
}
</style>
