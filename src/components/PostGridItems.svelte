<script>
  export let title;
  export let imageUrl;
</script>

<div class="container">
  <div class="image">
    <img src={imageUrl} alt={title} />
  </div>
  <h1>{title}</h1>
</div>

<style>
  @font-face {
    font-family: 'Muli';
    font-style: normal;
    font-weight: 400;
    font-display: swap;
    src: url(https://fonts.gstatic.com/s/muli/v27/7Aulp_0qiz-aVz7u3PJLcUMYOFnOkEk30e6fwniDtzM.woff)
      format('woff');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA,
      U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212,
      U+2215, U+FEFF, U+FFFD;
  }

  .container {
    background-color: #ffff;
    border-radius: 10px;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1), 0 6px 6px rgba(0, 0, 0, 0.1);
    padding: 50px 20px;
    text-align: center;
    max-width: 100%;
    width: 350px;
  }
  .image {
    width: 100%;
    height: 14rem;
  }
  .image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  h1 {
    font-family: 'Muli';
    font-size: 1.5rem;
    margin: 0.5rem 0;
    color: #e2b185;
    font-weight: bold;
  }
</style>
