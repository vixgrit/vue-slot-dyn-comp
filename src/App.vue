<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
                <br>
                <button @click="displayTemplate = 'appBlue'" class="btn btn-primary">Load Blue Template</button>
                <button @click="displayTemplate = 'appGreen'" class="btn btn-success">Load Green Template</button>
                <button @click="displayTemplate = 'appRed'" class="btn btn-danger">Load Red Template</button>
                <hr>
                <component :is="displayTemplate">
                  <h1>Default text here!</h1>
                </component>
            </div>
        </div>
    </div>
</template>

<script>
    import Blue from './components/Blue.vue';
    import Green from './components/Green.vue';
    import Red from './components/Red.vue';

    export default {
        components: {
            appBlue: Blue,
            appGreen: Green,
            appRed: Red
        },
        data() {
          return {
            displayTemplate: 'appBlue'
          }
        }
    }
</script>

<style>
</style>
