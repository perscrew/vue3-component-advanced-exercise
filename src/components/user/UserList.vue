<template>
  <user-item
    v-for="user in users"
    :key="user.id"
    :id="user.id"
    :firstName="user.firstName"
    :lastName="user.lastName"
    :age="user.age"
    @delete-user="openConfirm"
  ></user-item>

  <base-dialog
    v-if="isShowDialog"
    title="Confirmation"
    @close="isShowDialog = false"
  >
    <template #default>
      <p>Do you want to really remove this user ?</p>
    </template>
    <template #actions>
      <button @click="removeUser">Confirm</button>
    </template>
  </base-dialog>
</template>

<script>
import BaseDialog from '../UI/BaseDialog.vue';
import UserItem from './UserItem.vue';
export default {
  components: { UserItem, BaseDialog },
  inject: ['users'],
  data() {
    return {
      isShowDialog: false,
    };
  },
  methods: {
    openConfirm() {
      this.isShowDialog = true;
    },
    removeUser(id) {
      const userIndex = this.users.findIndex((user) => user.id === id);
      this.users.splice(userIndex, 1);
    },
  },
};
</script>