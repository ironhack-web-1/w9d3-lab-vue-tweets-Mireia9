<template>
  <div className="tweet">
    <ProfileImage :image="image" />

    <div className="body">
      <div className="top">
        <User :name="name" :handle="handle" />

        <TimeStamp :timestamp="timestamp" />
      </div>
        <Message :message="message" />
      
      <div className="actions">
        <ActionsComponent />      
      </div>
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>
<script>
import ProfileImage from "./ProfileImage.vue";
import User from "./User.vue";
import TimeStamp from "./TimeStamp.vue";
import Message from "./Message.vue";
import ActionsComponent from "./ActionsComponent.vue";
export default {
  props: ["name", "image", "handle", "timestamp", "message"],
  components: { ProfileImage, User, TimeStamp, Message, ActionsComponent },
};
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
