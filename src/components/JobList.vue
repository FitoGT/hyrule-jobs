<template>
  <div class="job-list">
    <p>
      Order By: {{ order }}
    </p>
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h2>{{ job.title }} in {{ job.location }}</h2>
        <div class="salary">
          <p>{{ job.salary }} rupees</p>
        </div>
        <div class="description">
          Hyrule approximately things virtually essentially Farore actually generally things fully relatively Sheik
          largely Hyrule ultimately begin things surely Great Fairy usually Majora obviously Nayru significantly perhaps
          specifically hardly slightly ok much so Boomerang significantly Darunia actual things rather significantly
          stuff most generally fully nicely most Master Sword certainly Triforce definitely
        </div>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import Job from '@/types/Job';
import OrderTerms from '@/types/OrderTerm';

export default defineComponent({
  props: {
    jobs: {
      required: true,
      type: Array as PropType<Job[]>
    },
    order: {
      required: true,
      type: String as PropType<OrderTerms>
    }
  }
})
</script>

<style scoped>
.job-list {
  max-width: 960px;
  margin: 40px auto;
}

.job-list ul {
  padding: 0;
}

.job-list li {
  list-style-type: none;
  background: white;
  padding: 16px;
  margin: 16px 0;
  border-radius: 4px;
}

.job-list h2 {
  margin: 0 0 10px;
  text-transform: capitalize;
}

.salary {
  display: flex;
}

.salary img {
  width: 30px;
}

.salary p {
  color: #17bf66;
  font-weight: bold;
  margin: 10px 4px;
}
</style>