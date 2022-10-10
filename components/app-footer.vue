<script setup>
const title = ref("footer");
</script>

<template>
  <div>
    <Head>
      <Title>{{ title }}</Title>
      <Meta name="description" :content="title" />
      <Style type="text/css" children="body { background-color: #262626; color: white; }" />
    </Head>

    <h1>{{ title }}</h1>
  </div>
</template>
