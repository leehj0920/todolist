<template>
	<div>
		<main class="todo">
			<div class="container">
				<h1>To - Do List</h1>

				<!-- ul.list_add -->
				<ul class="list_add">
					<li class="list_add_tit"><p>등록 하기</p></li>
					<li><p><input type="text"><button>등 록</button></p></li>
				</ul>
				<!--// ul.list_add -->  

				<!-- ul.todo_list -->
				<ul class="todo_list">
					<li class="todo_list_tit"><p>할 일</p></li>
					<li class="del_btn" v-for="item, index in todolist" :key="index">
						<p>
							<input type="checkbox" name="check1" value="">{{ item.todo }}
						</p>
					</li>
				</ul>
				<!--// ul.todo_list -->

			</div>
   		</main>

	</div>
</template>

<script>
export default {
  name: 'todolist',
  data: function() {
	  return {
		  todolist:[
			  {todo:"Vue.js공부하기"},
			  {todo:"과제하기"},
			  {todo:"엄마한테 전화하기"},
			  {todo:"예원이 수학 테스트"},
			  {todo:"운동하기"},
		  ]
	  }
  },
}
</script>
