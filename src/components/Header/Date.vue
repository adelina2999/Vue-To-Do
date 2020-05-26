<template>
  <div>
    <span class="date-align date-size">Today: {{ todayDate }}</span>
  </div>
</template>

<script>
import moment from 'moment'

export default {
	name: 'Date',
	data() {
		return {
			todayDate: ''
		}
	},
	created() {
		this.todayDate = moment().format('D MMM YYYY')
	}
}
</script>

<style>
	.date-align {
    position: absolute;
    top: 50px;
    right: 5px;
    text-align: right;
  }
  .date-size {
    font-size: 25px;
  }
</style>
