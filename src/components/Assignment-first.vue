<template>
  <div id="customer-details">
    <h2>Customer Details</h2>
    <div class="input-container">
      <input v-model="firstName" type="text" placeholder="Enter First Name" />
      <input v-model="lastName" type="text" placeholder="Enter Last Name" />
      <input v-model="address" type="text" placeholder="Enter Address" />
      <button @click="addCustomer">Add</button>
    </div>

    <table>
      <thead>
        <tr>
          <th>First Name</th>
          <th>Last Name</th>
          <th>Address</th>
          <th>Actions</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(customer, index) in customers" :key="index" :class="{ marked: customer.marked }">
          <td>{{ customer.firstName }}</td>
          <td>{{ customer.lastName }}</td>
          <td>{{ customer.address }}</td>
          <td>
            <button @click="removeCustomer(index)">❌</button>
            <button @click="toggleMark(index)">✔</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      address: "",
      customers: []
    };
  },
  methods: {
    addCustomer() {
      if (this.firstName && this.lastName && this.address) {
        this.customers.push({
          firstName: this.firstName,
          lastName: this.lastName,
          address: this.address,
          marked: false
        });
        this.firstName = "";
        this.lastName = "";
        this.address = "";
      }
    },
    removeCustomer(index) {
      this.customers.splice(index, 1);
    },
    toggleMark(index) {
      this.customers[index].marked = !this.customers[index].marked;
    }
  }
};
</script>

<style scoped>
#customer-details {
  font-family: Arial, sans-serif;
  width: 60%;
  margin: 20px auto;
  text-align: center;
}

.input-container {
  margin-bottom: 15px;
}

input {
  padding: 5px;
  margin: 5px;
}

button {
  padding: 5px 10px;
  cursor: pointer;
}

table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 10px;
}

th, td {
  border: 1px solid black;
  padding: 8px;
  text-align: left;

}

.marked {
  color: red;
  font-weight: bold;
}
</style>
