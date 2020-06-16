<template>
  <div class="card">
    <div class="card-content">
      <div class="content">
        <div class="level">
          <div class="level-left">
            <b-input v-model="description" :placeholder="placeholder" class="mr-3"></b-input>
            <b-select placeholder="Project" expanded>
              <option v-for="(item, index) in projects" :key="index" :value="item.id">{{item.name}}</option>
            </b-select>
          </div>
          <div class="level-right">
            <b-button type="is-danger" size="is-medium" style="min-width: 100px;" @click="startTimer">{{buttonText}}</b-button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TimerBar',
  data: () => ({
    description: "",
    timerRunning: false,
    timerStarted: null,
    placeholder: "What are you about to do?",
    projects: [
      { id: 1, name: 'Beamerstream' },
      { id: 2, name: 'Aeijijow' },
      { id: 3, name: 'Gwi' },
      { id: 4, name: 'Bdejgwjeij' },
      { id: 5, name: 'Rwehgnhnjaw' },
      { id: 6, name: 'Rherhiee' },
    ]
  }),
  computed: {
    buttonText(){
      return this.timerRunning?this.timerStarted:"Start"
    }
  },
  methods: {
    startTimer(){
      this.timerStarted = Date.now();
      this.timerRunning = true;
    }
  }
};
</script>

<style lang="scss" scoped>
</style>