<template>
  <h1>My Form</h1>
  <form @submit.prevent="handleSubmit">
    <label for="name">Name</label><br />
    <input v-model="name" type="text" name="" id="name" />
    <br />
    <br />
    <fieldset>
      <legend>Please select your favorite Web language:</legend>
      <input
        v-model="language"
        type="radio"
        id="html"
        name="fav_language"
        value="HTML"
      />
      <label for="html">HTML</label><br />
      <input
        v-model="language"
        type="radio"
        id="css"
        name="fav_language"
        value="CSS"
      />
      <label for="css">CSS</label><br />
      <input
        v-model="language"
        type="radio"
        id="javascript"
        name="fav_language"
        value="JavaScript"
      />
      <label for="javascript">JavaScript</label>
    </fieldset>
    <br />
    <input v-model="terms" type="checkbox" name="newsletter" id="terms" />
    <label for="terms">Do you accept the terms and conditions?</label>
    <br />
    <br />
    <button>Submit</button>
  </form>
  <br />
  <table>
    <tr>
      <td>Name</td>
      <td>{{ name }}</td>
    </tr>
    <tr>
      <td>Language</td>
      <td>{{ language }}</td>
    </tr>
    <tr>
      <td>Terms</td>
      <td>{{ terms }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      language: "",
      terms: false,
    };
  },
  methods: {
    handleSubmit() {
      this.$router.push("/results");
    },
  },
};
</script>

<style></style>
