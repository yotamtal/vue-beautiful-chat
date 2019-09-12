<template>
  <div class="conversation-list">
    <table class="" style="padding-top: 5px">
      <tbody>
        <tr v-for="conversation in conversations" :key="conversation.uri">
            <td style="text-align: center;"><img :src="conversation.user.avatar" class="img-msg"/></td>
            <td class="conversation-element">{{conversation.user.name}}</td>
        </tr>
      </tbody>
  </table>
  </div>
</template>
<script>
export default {
  props: {
    conversations: {
      type: Array,
      required: true
    }
  }
}
</script>
<style scoped>
  .conversation-list {
    height: 100%;
    overflow: auto;
    padding-left: 5px;
    padding-top: 8px;
  }
  .img-msg {
    border-radius: 50%;
    width: 50px;
    margin-right: 5px;
  }
  .conversation-element {
    font-size: 20px;
    vertical-align: middle;
  }
</style>
