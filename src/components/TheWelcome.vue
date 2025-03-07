<template>
  <div>
    <table border="1">
      <thead>
        <tr>
          <th>Name</th>
          <th>Salary</th>
          <th>Age</th>
          <th>Action</th>
          <th>Edit</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(user, index) in users" :key="user.id">
          <td>{{ user.name }}</td>
          <td>{{ user.salary }}</td>
          <td>{{ user.age }}</td>
          <td>
            <a href="#" @click="removeUser(index)">Delete</a>
          </td>
          <td>
            <a href="#" @click="editUser(index)">Edit</a>
          </td>
        </tr>
      </tbody>
    </table>

    <!-- Modal for Editing -->
    <div v-if="isEditing" class="modal">
      <div class="modal-content">
        <h3>Edit User</h3>
        <form @submit.prevent="saveChanges">
          <label for="name">Name:</label>
          <input type="text" v-model="editedUser.name" />

          <label for="salary">Salary:</label>
          <input type="number" v-model="editedUser.salary" />

          <label for="age">Age:</label>
          <input type="number" v-model="editedUser.age" />

          <button type="submit">Save</button>
          <button @click="cancelEdit">Cancel</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: 'name1', salary: 100, age: 30 },
        { id: 2, name: 'name2', salary: 200, age: 40 },
        { id: 3, name: 'name3', salary: 300, age: 50 },
      ],
      isEditing: false,
      editedUser: null,
      editedUserIndex: null,
    };
  },
  methods: {
    removeUser(index) {
      this.users.splice(index, 1);
    },
    editUser(index) {
      this.isEditing = true;
      this.editedUserIndex = index;
      this.editedUser = { ...this.users[index] };
    },
    saveChanges() {
      if (this.editedUser) {
        this.users[this.editedUserIndex] = { ...this.editedUser };
        this.cancelEdit();
      }
    },
    cancelEdit() {
      this.isEditing = false;
      this.editedUser = null;
      this.editedUserIndex = null;
    },
  },
};
</script>

<style>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal-content {
  background: white;
  padding: 20px;
  border-radius: 8px;
  width: 300px;
}

button {
  margin-top: 10px;
}
</style>