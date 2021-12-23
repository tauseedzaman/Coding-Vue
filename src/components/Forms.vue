<template>
  <h1>Vue Forms Test</h1>

  <span>Multiline message is:</span>
  <p style="white-space: pre-line">{{ message }}</p>
  <br />
  <textarea v-model="message" placeholder="add multiple lines"></textarea>
  <hr />
  <br />
  <label for="checkbox"
    >At is check or not <span class="text-danger">{{ checked }}</span></label
  >
  <center>
    <input type="checkbox" id="checkbox" v-model="checked" class="form-check" />
  </center>
  <hr />
  <br />
  <div id="v-model-multiple-checkboxes">
    <input type="checkbox" id="jack" value="Jack" v-model="checkedNames" />
    <label for="jack">Jack</label><br />
    <input type="checkbox" id="john" value="John" v-model="checkedNames" />
    <label for="john">John</label><br />
    <input type="checkbox" id="mike" value="Mike" v-model="checkedNames" />
    <label for="mike">Mike</label>
    <br />
    <span>Checked names: {{ checkedNames }}</span>
  </div>
  <br />
  <hr />
  <div id="v-model-radiobutton">
    <input type="radio" id="one" value="One" v-model="picked" />
    <label for="one">One</label>
    <br />
    <input type="radio" id="two" value="Two" v-model="picked" />
    <label for="two">Two</label>
    <br />
    <span>Picked: {{ picked }}</span>
  </div>
  <br />
  <hr />
  <div id="v-model-select-dynamic" class="demo">
    <select v-model="selected">
      <option v-for="option in options" :value="option.value" :key="option.text">
        {{ option.text }}
      </option>
    </select>
    <span>Selected: {{ selected }}</span>
  </div>
  <br>
  <hr>
  <input type="checkbox" v-model="toggle" true-value="yes" false-value="no" />
</template>

<script>
export default {
  data() {
    return {
      message: "",
      checked: false,
      checkedNames: [],
      picked: false,
      options: [
        { text: "One", value: "A" },
        { text: "Two", value: "B" },
        { text: "Three", value: "C" },
      ],
      toggle:"no"
    };
  },
};
</script>

<style>
</style>