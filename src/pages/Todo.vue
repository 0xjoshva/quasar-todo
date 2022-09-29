<template>
  <q-page class="bg-grey-3 column">
    <q-list separator bordered>
      <q-item class="bg-white" @click="task.done = !task.done" v-for="task in tasks" :key="task.title" tag="label" v-ripple clickable>
        <q-item-section avatar>
          <q-checkbox class="no-pointer-events" v-model="task.done"  color="primary"/>
        </q-item-section>
        <q-item-section>
          <q-item-label>{{task.title}}</q-item-label>
        </q-item-section>
      </q-item>
    </q-list>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      tasks: [
        {
          title: "Wake Up",
          done: false,
        },
        {
          title: "Eat Breakfast",
          done: true,
        },
        {
          title: "Take Shower",
          done: false,
        },
      ],
    };
  },
};
</script>
