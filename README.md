# Bebsite-To-Do-List-with-Vue
more detals in README
Vue comands in my file:
__const { createApp, ref } = Vue;
## Destructuring: extracts createApp and ref from the Vue object.
__createApp({
## Creates a Vue application instance.
__setup() {
## Composition API entry point. Defines reactive data and methods.
__const newTask = ref('');
##Creates reactive variable `newTask` (initial value empty string).
__const tasks = ref(['Сделать сальто', 'Прыгнуть выше головы']);
## Creates reactive array `tasks` with two initial to-do items.
__function addTask() {
## Function that adds new task to the array.
__if (newTask.value.trim() !== '') {
          tasks.value.push(newTask.value);
          newTask.value = '';
        }
## Checks non-empty → pushes to array → clears input field.
}
__function removeTask(index) {
## Removes task at given index from array.
__tasks.value.splice(index, 1);
## Removes one item from array at specified index.
}
__return { newTask, tasks, addTask, removeTask };
## Exposes data and methods to template.
}
__}).mount('#app');
## Mounts Vue app to HTML element with id="app".
