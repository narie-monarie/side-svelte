<script>
  export let filter;
</script>

<div class="mx-auto container my-7 items-center">
  <div>
    <h1 class="mt-10 mb-4 text-center text-2xl">List of Users</h1>
  </div>
  <select
    on:change={filter}
    name="user-filter"
    id="user-filter"
    class="border rounded-lg px-4 py-2 ml-2"
  >
    <option value={null}>All</option>
    <option value={true}>Active</option>
    <option value={false}>Inactive</option>
  </select>
</div>
