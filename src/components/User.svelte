<script>
  export let user;
  export let i;
</script>

<main>
  <div />
  <div
    class="flex items-center m-5 bg-white border p-2 rounded-lg shadow-md hover:shadow-lg cursor-pointer"
  >
    <p class="w-10">{i + 1}</p>
    <img class="rounded-full w-20 h-20 " src={user.image} alt="svg shit" />
    <p class="mx-4 w-20">{user.name}</p>
    <p class="mx-4 w-20">{user.email}</p>
  </div>
</main>
