<script context="module">
  import PostGrid from '../components/PostGrid.svelte';
  import { request, gql } from 'graphql-request';
  import Highlight from '../components/Highlight.svelte';

  const endpoint = 'https://api-bridal.herokuapp.com/graphql';

  const query = gql`
    {
      posts {
        id
        title
        subtitle
        description
        post
        imageUrl
      }
    }
  `;

  export const load = async () => {
    const data = await request(endpoint, query);

    return {
      props: {
        data,
      },
    };
  };
</script>

<script>
  export let data;
</script>

<Highlight
  title={data.posts[data.posts.length - 1].title}
  description={data.posts[data.posts.length - 1].description}
  imageUrl={data.posts[data.posts.length - 1].imageUrl}
  post={data.posts[data.posts.length - 1].post}
/>
<PostGrid albums={data.posts} />
