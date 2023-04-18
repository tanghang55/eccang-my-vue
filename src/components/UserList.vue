<template>
    <div class="user-list-page">
      <h2 class="user-list-title">User List</h2>
      <table class="user-table">
        <thead>
          <tr>
            <th>ID</th>
            <th>Name</th>
            <th>Email</th>
            <th>Role</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="user in userList" :key="user.id">
            <td>{{ user.id }}</td>
            <td>{{ user.name }}</td>
            <td>{{ user.email }}</td>
            <td>{{ user.role }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        userList: [
          { id: 1, name: 'Alice', email: 'alice@example.com', role: 'Admin' },
          { id: 2, name: 'Bob', email: 'bob@example.com', role: 'User' },
          { id: 3, name: 'Charlie', email: 'charlie@example.com', role: 'User' },
          { id: 4, name: 'David', email: 'david@example.com', role: 'User' },
        ],
      }
    },
  }
  </script>
  
  <style>
  .user-list-page {
    padding: 40px;
  }
  
  .user-list-title {
    font-size: 28px;
    font-weight: 600;
    margin-top: 0;
    margin-bottom: 30px;
  }
  
  .user-table {
    width: 100%;
    border-collapse: collapse;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  
  thead tr {
    background-color: #f9f9f9;
    font-weight: 600;
  }
  
  thead th {
    padding: 10px;
    text-align: left;
  }
  
  tbody tr:nth-child(even) {
    background-color: #f5f5f5;
  }
  
  tbody td {
    padding: 10px;
    border: 1px solid #ccc;
  }
  </style>
  