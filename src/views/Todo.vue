<template>
    <div class="pa-5">
        <v-list
        flat
        subheader
        three-line
        >
        <div>
            <v-btn
                class="mx-2"
                fab
                dark
                color="indigo"
                >
                <v-icon dark>
                    mdi-plus
                </v-icon>
            </v-btn>
            <v-btn
                class="mx-2"
                fab
                dark
                color="cyan"
                >
                <v-icon dark>
                    mdi-pencil
                </v-icon>
            </v-btn>
        </div>
        <v-subheader>General</v-subheader>

        <v-list-item-group
            v-model="settings"
            multiple
            active-class=""
        >
            <v-list-item v-for="task,index in tasks" :key="index">
            <template v-slot:default="{ active }">
                <v-list-item-action>
                <v-checkbox :input-value="active" v-model="check"></v-checkbox>
                </v-list-item-action>
                <v-list-item-content>
                <v-list-item-title>{{task.title}}</v-list-item-title>
                <v-list-item-subtitle>{{task.content}}</v-list-item-subtitle>
                </v-list-item-content>
            </template>
            </v-list-item>
        </v-list-item-group>
        </v-list>
    </div>
</template>

<script>
export default {
    data(){
        return{
            tasks:[
                {   
                    title: "Mai thai duong",
                    content: "sadfjklasjd;f"
                },
                {
                    title: "Ta duc chien",
                    content: "Dkjashfjkahslf"
                }
            ]
        }
    },
    methods:{
        
    }
}
</script>