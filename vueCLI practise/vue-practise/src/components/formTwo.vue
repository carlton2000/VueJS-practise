    <template>
  <div >
      <div slot="form-header">
      <h3> This is the title of form TWo</h3>
      <p> Information about th form </p>
      </div>
      <div slot="form-fields">
        <input type="text" placeholder="name" required />
        <input type="password" placeholder="password" required />
      </div>
      <div slot="form-controls">
        <button v-on:click="handleSubmit">Submit</button>
      </div>
      <div id="useful-links">
              <ul>
                  <li><a href="">Link 1</a></li>
                  <li><a href="">Link 2</a></li>
                  <li><a href="">Link 3</a></li>
                  <li><a href="">Link 4</a></li>
              </ul>
          </div>
  </div> 
</template>

<script>


export default{
  components:{

  },
  data(){
        return{
            
        }
    },
}
</script>

<style>
h1{
    text-align: center;
}
form{
    width: 100%;
    max-width: 960px;
    margin: auto;
}
#useful-links ul{
    padding:0;
}
#useful-links li{
    display:inline-block;
    margin-right: 10px;
}

form > div {
    padding: 20px;
    background: rgb(126, 123, 123);
    margin: 20px 0;
}
#form-header{
    background: grey;
    border: 1px solid rgb(85, 72, 72);
}
</style>