<template>
	<div>
		<div :key="task.id" v-for="task in tasks">
			<TaskComponent @toogle-reminder="$emit('toogle-reminder', task.id)" @delete-task="$emit('delete-task', task.id)" :task="task" />
		</div>
	</div>
</template>

<script>
import TaskComponent from './Task.vue'

export default {
	name: "TasksComponent",
	props: {
		tasks: Array,
	},
	components: {
		TaskComponent
	},
	emits: ['toogle-reminder', 'delete-task'],
}
</script>