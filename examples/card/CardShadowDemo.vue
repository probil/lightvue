<template>
  <div class="card-demo-wrapper">
    <div class="card-demo">
      <LvCard> <div v-html="dummyContent('default (style 1)')"></div> </LvCard>
    </div>
    <div class="card-demo">
      <LvCard :shadowStyle="1"> <div v-html="dummyContent('shadowStyle = 1')"></div> </LvCard>
    </div>
    <div class="card-demo">
      <LvCard :shadowStyle="2"> <div v-html="dummyContent('shadowStyle = 2')"></div> </LvCard>
    </div>
    <div class="card-demo">
      <LvCard :shadowStyle="3"> <div v-html="dummyContent('shadowStyle = 3')"></div> </LvCard>
    </div>
    <div class="card-demo">
      <LvCard :shadowStyle="4"> <div v-html="dummyContent('shadowStyle = 4')"></div> </LvCard>
    </div>
    <div class="card-demo">
      <LvCard :shadowStyle="5"> <div v-html="dummyContent('shadowStyle = 5')"></div> </LvCard>
    </div>
    <div class="card-demo">
      <LvCard :shadowStyle="0"> <div v-html="dummyContent('shadowStyle = 0')"></div> </LvCard>
    </div>
  </div>
</template>

<script>
import LvCard from 'lightvue/card';

export default {
  data() {
    return {};
  },
  methods: {
    dummyContent(propValue) {
      return `<div>
                <h4><span>PROP: </span>${propValue}</h4>
                <p>
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                </p>
            </div>`;
    },
  },
  components: {
    LvCard,
  },
};
</script>

<style>
.card-demo-wrapper {
  display: flex;
  flex-flow: row wrap;
  justify-content: flex-start;
}

.card-demo {
  height: 400px;
  width: 300px;
  margin: 30px;
}

.card-demo h4 > span {
  font-size: 0.9em;
  opacity: 0.8;
  font-weight: lighter;
}

@media (max-width: 500px) {
  .card-demo h4 > span {
    display: block;
  }
}

.card-demo p {
  margin-top: 30px;
  opacity: 0.8;
}
</style>
