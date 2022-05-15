<script>
  import PostGridItems from './PostGridItems.svelte';
  export let albums;
</script>

<section id="albums">
  {#each albums as album}
    <PostGridItems
      id={album.id}
      title={album.title}
      imageUrl={album.imageUrl}
    />
  {/each}
</section>

<style>
  section {
    width: 100%;
    box-sizing: border-box;
    padding: 10px;
    display: grid;
    grid-template-columns: 1fr;
    grid-gap: 1rem;
    margin-bottom: 4rem;
  }
  @media (min-width: 768px) {
    section {
      grid-template-columns: repeat(3, 1fr);
    }
  }
</style>
