<script lang="ts" setup>
import DownIcon from '../assets/icons/DownIcon.vue'
import UpIcon from '../assets/icons/UpIcon.vue'
defineProps({
  label: {
    type: String,
    required: true
  },
  username: {
    type: String,
    required: true
  },
  timeAgo: {
    type: String,
    required: true
  },
  urlImage: {
    type: String,
    required: true
  }
})
</script>
<template>
  <article>
    <aside>
      <slot name="image"> </slot>
    </aside>
    <div class="container">
      <header>
        <strong>{{ username }}</strong
        >20 hours ago
      </header>
      <p>
        {{ label }}
      </p>
      <footer>
        <span><UpIcon class="cursor-pointer" />2 <DownIcon class="cursor-pointer" /></span>
        <span class="cursor-pointer">Reply</span>
        <span class="cursor-pointer">Report</span>
      </footer>
    </div>
  </article>
</template>

<style lang="css" scoped>
article {
  display: flex;
  flex-direction: row;
  justify-content: stretch;
  align-items: stretch;
  flex-wrap: nowrap;
  gap: 24px;
}
header {
  font-size: 14px;
  line-height: 28px;
  font-weight: bold;
  color: #00000070;
}
header strong {
  font-weight: bold;
  color: #000000;
  font-size: 16px;
  margin-right: 10px;
}
article img {
  width: 60px;
  height: 60px;
}
aside {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  align-items: center;
  justify-content: start;
  gap: 10px;
}
hr {
  border: 1px solid #00000050;
  width: 1px;
  height: 80%;
}
.cursor-pointer {
  cursor: pointer;
}

.container {
  display: flex;
  flex-direction: column;
  flex-wrap: nowrap;
  gap: 10px;
  overflow-x: auto;
}
*::-webkit-scrollbar {
  height: 4px;
  width: 10px;
  scrollbar-gutter: auto;
}

*::-webkit-scrollbar-track {
  border-radius: 20px;
}

*::-webkit-scrollbar-thumb {
  border-radius: 20px;
  background: #888;
}

*::-webkit-scrollbar-thumb:hover {
  background: #555;
}
p {
  font-size: 14px;
  line-height: 28px;
  font-weight: lighter;
  color: #00000095;
}
footer {
  display: flex;
  gap: 30px;
}
footer span {
  display: flex;
  gap: 10px;
  align-items: center;
}
</style>
