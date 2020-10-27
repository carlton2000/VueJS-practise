<template>
    <div id="show-blogs">
        <h1>List Blog Titles</h1>
        <input type="text" v-model="search" placeholder="search blogs" />
        <div v-for="blog in filteredBlogs" :key="blog" class="single-blog">
            <h2 v-rainbow>{{ blog.title | to-uppercase }}</h2>
            
        </div>
    </div>
</template>

<script>
import searchmxin from '../mxins/searchmxin'

export default {
    data () {
        return {
            blogs: [],
            search: ''
        }
    },
    methods: {
    },
    created() {
        this.$http.get('http://jsonplaceholder.typicode.com/posts').then(function(data){
            this.blogs = data.body.slice(0,10);
        });
    },
    computed: {

    },
    filters:{
        toUppercase(value){
            return value.toUpperCase();
        }
    },
    directives:{
        'rainbow':{
            bind(el, binding, vnode){
           el.style.color = "#" + Math.random().toString(16).slice(2,8);
     }
    }
   },
     mixins:[searchmxin]
}
</script>

<style scoped>
#show-blogs{
    max-width: 800px;
    margin: 0px auto;
}
.single-blog{
    padding: 20px;
    margin: 20px 0;
    box-sizing: border-box;
    background: rgb(122, 121, 121);
}
</style>
