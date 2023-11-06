<script lang="ts" setup>
import MessageComponent from './MessegeComponent.vue'
</script>
<template>
  <section>
    <div>
      <hr />
      <MessageComponent
        username="adamsdavid"
        time-ago="20 hours ago"
        label="I genuinely think that Codewell's community is AMAZING. It's just starting out but the templates on there are amazing"
        urlImage="avatar4.png"
      >
        <template #image>
          <img src="../assets/avatars/avatar4.png" alt="avatar" />
        </template>
      </MessageComponent>
      <div>
        <hr />

        <MessageComponent
          username="saramay"
          time-ago="16 hours ago"
          label="I agree. I've been coding really wel (pun intended) ever since I started practicing on their templates hehe."
          url-image="../assets/avatars/avatar1.png"
        >
          <template #image>
            <img src="../assets/avatars/avatar1.png" alt="avatar" />
          </template>
        </MessageComponent>
        <div>
          <hr />

          <MessageComponent
            username="jessica21"
            time-ago="114 hours ago"
            label="Okay, this comment wins"
            url-image="avatar2.png"
          >
            <template #image>
              <img src="../assets/avatars/avatar2.png" alt="avatar" />
            </template>
          </MessageComponent>
        </div>
      </div>
    </div>

    <div>
      <hr />

      <MessageComponent
        username="andrew231"
        time-ago="20 hours ago"
        label="Thanks for making this, super helpful"
        url-image="avatar3.png"
      >
        <template #image>
          <img src="../assets/avatars/avatar3.png" alt="avatar" />
          <hr />
        </template>
      </MessageComponent>
    </div>
  </section>
</template>

<style lang="css" scoped>
@media (max-width: 700px) {
  .text {
    font-size: 16px;
  }
}
div {
  position: relative;
  overflow: hidden;
  margin-top: 20px;
}
hr {
  position: absolute;
  width: 2px;
  background: #000;
  height: 100%;
  top: 70px;
  left: 23px;
}
img {
  width: 50px;
  height: 50px;
}
section {
  width: 70%;
  background: white;
  border-radius: 16px;
  padding: 50px 30px;
}

div > div {
  margin-left: 50px;
}
</style>
