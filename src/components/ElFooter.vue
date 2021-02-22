<template>
  <div>
    <footer class="footer">
      <p>
        ©
        {{ currentYear }}
      </p>
        <div class="spaces-contact">
        <a target="_blank" :href="`mailto:info@spaces.io`"
            >info@spaces.io</a
        >
        </div>
    </footer>
  </div>
</template>

<script>
import moment from "moment";

export default {
  name: 'el-footer',
  data() {
    return {
      currentYear: moment().year(),
    };
  },
};
</script>

<style scoped>
.footer {
    padding: 2rem 6%;
    background:var(--primaryFour);
    color: var(--semanticOne);
    font-size: 2rem;
    font-weight: 500;
    display: flex;
    flex-wrap: wrap;
}
p {
    margin: 0;
    margin-right: 2rem;
}
.spaces-contact {
    display: flex;
    align-items: center;
    flex: 1;
    justify-content: flex-end;
}
.spaces-contact a {
    color: var(--semanticOne);
}
</style>
