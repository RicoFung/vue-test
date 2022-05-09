<script>
export default {
  data() {
    return { info: {} };
  },
  methods: {
    getPosts() {
      const requestOptions = {
        method: "POST",
        headers: {
          "Content-Type": "application/json",
          Authorization:
            "Bearer eyJraWQiOiI4ZWU4MGU1OC0wMWRkLTRiZTMtYjcwZi0zOGQ0ZGI1ZjhmZGMiLCJhbGciOiJSUzI1NiJ9.eyJzdWIiOiJhZG1pbiIsImF1ZCI6InJpY28tY2xpZW50IiwibmJmIjoxNjUyMDk4Nzk2LCJzY29wZSI6WyJ0ZXN0LnJlYWQiXSwiaXNzIjoiaHR0cDpcL1wvYXV0aC1zZXJ2ZXI6OTAwMCIsImV4cCI6MTY1MjA5OTA5NiwiaWF0IjoxNjUyMDk4Nzk2fQ.MzLykcQU9ok49Fe3TiXgxYoWY1AcKMMnpAC4Kg_sAjGqW_sZ-1ZhHIdqKl0fEvetd0_KmRN41lZIzjzTVtEwvX6Ui7LjGU98HU57aD-9XBMClhtdYybpnFZV7OMkpNeEd9NWZdZjYVXhEe3YWClIzCOiKXyLEqiX8-SJO4ahWrY_dA0cg5ZGdc0hjVUuyGydzkDgIvXxXQ_pLuLk0LTJ3Al5ippUUpYGpHLNT6S5ojad-_NjiNDibB4eHVnweBZTW3mp9MO1dPnELWPNh2VYFhLTJkFszb4h4kI39Gnvzwund18I3Z7BFBynSMvUn_xFXeez6hJL3JQla5qeloeNoQ",
        },
      };
      fetch("/apis/test/hi", requestOptions)
        .then((response) => response.json())
        .then((data) => (this.info = data));
    },
  },
};
</script>

<template>
  <div class="about">
    <h1>This is an about page</h1>
  </div>
  <button @click="getPosts">Show Posts</button>
  <div>
    {{ info }}
  </div>
</template>
