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
  @font-face {
    font-family: 'Playfair Display SC';
    font-style: normal;
    font-weight: 400;
    src: url(https://fonts.gstatic.com/s/playfairdisplaysc/v15/ke85OhoaMkR6-hSn7kbHVoFf7ZfgMPr_lbkMEOE1I4o.woff2)
      format('woff2');
    unicode-range: U+0000-00FF, U+0131, U+0152-0153, U+02BB-02BC, U+02C6, U+02DA,
      U+02DC, U+2000-206F, U+2074, U+20AC, U+2122, U+2191, U+2193, U+2212,
      U+2215, U+FEFF, U+FFFD;
  }

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

  .text-container p h3 {
    font-family: 'Muli';
  }
  .image {
    width: 40%;
  }
  .image img {
    width: 100%;
    border-radius: 8px;
  }
</style>
