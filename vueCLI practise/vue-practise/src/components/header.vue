<template>
    <nav>
        <ul>
            <li><router-link to="/" exact>Blog</router-link></li>
            <li><router-link to="/add" exact>Add a new Blog</router-link></li>
        </ul>
    </nav>
</template>

<script>
// import searchmxin from '../mxins/searchmxin'

export default {
    data () {
        return {
            
        }
    },
    methods: {
    },
    
    computed: {

    },
    
}
</script>

<style scoped>
ul{
    list-style-type: none;
    text-align: center;
    margin: 0;
}
li{
    display: inline;
    margin: 0 10px;
}
a{
    color: #fff;
    text-decoration: none;
    padding: 6px 8px;
    border-radius: 10px;
}
nav{
    background: #444;
    padding: 14px 0;
    margin-bottom: 40px;
}
.router-link-active{
    background: lightgray;
    color: darkgrey;
}
</style>