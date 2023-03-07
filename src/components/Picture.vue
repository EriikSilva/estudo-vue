<template>
  <div>
    <img src="avatar" :alt="descricao" />
  </div>
</template>

<script>
export default {
  name: "Picture",
  data() {
    return {
      avatar: "../img/aaa.png",
      descricao: "Erik Felipe",
    };
  },
};
</script>
