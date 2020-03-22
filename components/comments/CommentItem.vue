<template>
  <div class="comment">
    <avatar :src="user.avatar"/>
    <div>
      <div class="username">
        {{ user.username }}
      </div>
      <div class="comment-body">
        {{ comment.message }}
      </div>
      <div>
        <font-awesome-icon class="text-primary" icon="heart"/> Gefällt mir
      </div>
    </div>
    <div class="sub-comment-list">
    </div>
  </div>
</template>

<script>
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import Avatar from '~/components/user/Avatar'

export default {
  components: {
    FontAwesomeIcon,
    Avatar
  },
  props: {
    comment: {
      type: Object,
      required: true
    }
  },
  computed: {
    user () {
      return this.comment.user
    },
    subComments () {
      if (Array.isArray(this.comment.subComments)) {
        return this.comment.subComments
      }
      return this.comment.subComments
    },
    imgUrl () {
      return '/avatar/' + this.user.avatar
    }
  }
}
</script>

<style lang="scss">
@import '../../assets/style/variables';

  .comment {
    display: grid;
    grid-template-columns: 4em auto;

    .avatar {
      margin-right: 0.2em;
    }
    .username {
      color: $primary;
      font-weight: 800;
    }
    .sub-comment-list {
      margin-left: 1em;
    }
  }
</style>
