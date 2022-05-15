<script>
  export let title;
  export let description;
  export let imageUrl;
  export let post;
</script>

<section class="grid-container">
  <div class="container">
    <div class="text-container">
      <h1 class="title">{title}</h1>
      <h3 class="description">{description}</h3>
      <p>{post}</p>
    </div>
    <div class="image">
      <img src={imageUrl} alt={title} />
    </div>
  </div>
</section>

<style>
  .grid-container {
    width: 100%;
    box-sizing: border-box;
    padding: 10px;
    margin-bottom: 4rem;
  }
  .container {
    display: flex;
    flex-direction: row;
    background-color: #ffff;
    border-radius: 10px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1), 0 6px 6px rgba(0, 0, 0, 0.1);
    padding: 50px 20px;
  }
  .text-container {
    padding-left: 1rem;
    width: 500px;
  }
  .text-container p {
    width: 400px;
  }
  .title {
    font-family: 'Playfair Display SC', Georgia, 'Times New Roman', Times, serif;
    font-size: 3rem;
    color: #807e7e;
    line-height: 1;
    font-weight: 400;
    margin-bottom: 1rem;
  }
  .image {
    width: 40%;
  }
  .image img {
    width: 100%;
    border-radius: 8px;
  }
</style>
