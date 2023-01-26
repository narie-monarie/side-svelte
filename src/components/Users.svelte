<script>
  import user1 from "../assets/img1.png";
  import user2 from "../assets/img2.png";
  import user3 from "../assets/img3.png";
  import FilterUser from "./FilterUser.svelte";
  import User from "./User.svelte";
  let users = [
    {
      id: 1,
      image: user1,
      name: "John",
      email: "John@bitfumes.com",
      active: false,
    },

    {
      id: 2,
      image: user2,
      name: "James",
      email: "James@bitfumes.com",
      active: true,
    },

    {
      id: 3,
      image: user3,
      name: "Jared",
      email: "Jared@bitfumes.com",
      active: false,
    },
  ];

  let filteredUsers = users;

  const filter = (e) => {
    if (e.target.value === "null") {
      filteredUsers = users;
      return;
    }
    const status = e.target.value === "true";
    filteredUsers = users.filter((user) => user.active === status);
  };
</script>

<main>
  <FilterUser {filter} />
  <div>
    {#each filteredUsers as user, i (user.id)}
      <User {user} {i} />
    {:else}
      <p>User Not Found</p>
    {/each}
  </div>
</main>

<style>
</style>
