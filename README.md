# Bebsite-To-Do-List-with-Vue
more detals in README
Vue comands in my file:
## Destructuring: extracts createApp and ref from the Vue object.
__const { createApp, ref } = Vue;
## Creates a Vue application instance.
__createApp({
## Composition API entry point. Defines reactive data and methods.
__setup() {
## Creates reactive variable `newTask` (initial value empty string).
__const newTask = ref('');
## Creates reactive array `tasks` with two initial to-do items.
__const tasks = ref(['Сделать сальто', 'Прыгнуть выше головы']);
## Function that adds new task to the array.
__function addTask() {
## Checks non-empty → pushes to array → clears input field.
__if (newTask.value.trim() !== '') {
          tasks.value.push(newTask.value);
          newTask.value = '';
        }
        
}        
## Removes task at given index from array.
__function removeTask(index) {
## Removes one item from array at specified index.
__tasks.value.splice(index, 1);

}
## Exposes data and methods to template.
__return { newTask, tasks, addTask, removeTask };

}
## Mounts Vue app to HTML element with id="app".
__}).mount('#app');
===2===
## A reusable Vue component defined with its own template and logic.
__const ChildComponent
## Local registration, making the component available only inside the parent component’s template.
__components: { ChildComponent }
## Custom HTML tag that renders the ChildComponent instance in the parent template.
__<child-component></child-component>
## setup() is the entry point for Composition API
__setup() {
## ref creates a reactive variable that automatically updates the UI when changed.
__const count = ref(0);
