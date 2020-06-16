<template>
  <section class="section">
    <div class="columns is-fluid">
      <div class="column">
        <div class="card">
          <div class="card-content">
            <div class="content">
              <div class="level">
                <div class="level-left">
                  <b-input v-model="description" :placeholder="placeholder" size="is-medium" style="width: 500px"></b-input>
                </div>
                <div class="level-right">
                  <b-button type="is-danger" size="is-medium" @click="startTimer">00:00</b-button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "HomePage",
  data: () => ({
    description: "",
    placeholder: "What are you about to do?"
  }),
  methods: {
    startTimer(){
      alert("hi");
    }
  }
};
</script>
