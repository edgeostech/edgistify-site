<template>
  <div class="resource-container">
    <Blog />
    <Media />
    <CaseStudy />
    <Video />
    <EdgistifyForm />
  </div>
</template>

<script>
import Blog from "../../components/Resources/Blog/Blog.vue"
import Media from "../../components/Resources/Media/Media.vue";
import CaseStudy from "../../components/Resources/CaseStudy/CaseStudy.vue"
import Video from "../../components/Resources/Video/Video.vue"
import EdgistifyForm from "../../components/EdgistifyForm/EdgistifyForm.vue";

export default {
  components: {
    Blog,
    Media,
    CaseStudy,
    Video,
    EdgistifyForm
  },
  setup () { },
  head() {
    return {
      title: "Access The Tools You Need to Learn Resources Edgistify"
    };
  }
};
</script>

<style lang="scss" scoped>
.resource-container {
  display: flex;
  width: 100%;
  height: auto;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  // margin-left: 100px;
}
</style>