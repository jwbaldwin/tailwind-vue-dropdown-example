<template>
  <main-dropdown>
    <template>
      <img src="../assets/profile.png" alt="profile image">
      <div>
        <ul>
          <li>
            <a to="/profile">
              <div>{{ username }}</div>
              <div>{{ email }}</div>
            </a>
          </li>
          <li>
            <a to="/profile">Profile</a>
          </li>
          <li>
            <a>Sign out</a>
          </li>
        </ul>
      </div>
    </template>
  </main-dropdown>
</template>

<script>
import MainDropdown from "@/components/MainDropdown";
export default {
  name: "button-with-dropdown",
  data() {
    return {
      username: "John Wick",
      email: "dontkillmydog@johnwick.com"
    };
  },
  components: { MainDropdown }
};
</script>