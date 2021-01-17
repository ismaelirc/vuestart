<template>
  <div>
    <h1>Minha lista</h1>
    <button @click="() => showList = !showList" >Ver lista</button>

    <ul v-if="showList">
        <li
            v-for="(task, index) in tasks" 
            :key="`${task}-${index}`"
        >
            {{task.name}}
        </li>
    </ul>
    <p v-else>Lista de tarefas escondidas</p>

  </div>
</template>

<script>
export default {
    data: () => ({
        showList: false,
        tasks:[
            {name: 'Fazer o curso', isDone: false}
        ]
    })
}
</script>