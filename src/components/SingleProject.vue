<template>
<div class="project">
    <div class="actions">
        <h3 @click="show">{{project.title}}</h3>
        <div class="icons">
            
            
            <span class="material-icons-outlined">done</span>
        </div>
        
    </div>
    <div v-if="showdetails" class="details">
        <p>{{project.details}}</p>
    </div>

</div>
    
</template>
<script>
export default {
    props:['project'],
    data()
    {
        return{
            showdetails:false
        }
    },
    methods:{
        show()
        {
            this.showdetails=!this.showdetails;
        }
    }
    
}
</script>
<style>
.project{
    margin: 20px auto;
    background: white;
    padding: 10px 10px;
    border-radius: 3px;
    box-shadow: 2px 3px 2px rgba(0,0,0,0.5);
    border-left: 4px solid rgb(233, 9, 173);
}
h3{
    cursor: pointer;
}
</style>


