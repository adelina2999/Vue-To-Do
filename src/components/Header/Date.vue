<template>
  <div>
    <span>Today: {{ todayDate }}</span>
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
		this.todayDate = moment().format('MMM Do YY')
	}
}
</script>

<style>

</style>
