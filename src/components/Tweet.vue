<template>
  <div className="tweet">
    <ProfileImage :image="image" />

    <div className="body">
      <div className="top">
        <User :name="name" :handle="handle" />

        <TimeStamp :timestamp="timestamp" />
      </div>

      <p className="message">
        {{ message }}
      </p>

      <div className="actions">
        <!-- Font Awesome icons -->
        <i class="far fa-comment"></i>
        <i class="fas fa-retweet"></i>
        <i class="far fa-heart"></i>
        <i class="fas fa-share"></i>
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>
<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import TimeStamp from "./TimeStamp.vue";
export default {
  props: ["name", "image", "handle", "timestamp", "message"],
  components: { ProfileImage, User, TimeStamp },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
