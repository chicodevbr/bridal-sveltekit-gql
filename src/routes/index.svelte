<script context="module">
  import HeaderBar from '../components/UI/HeaderBar.svelte';
  import PostGrid from '../components/PostGrid.svelte';
  import { request, gql } from 'graphql-request';

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

<HeaderBar />

<PostGrid albums={data.posts} />
