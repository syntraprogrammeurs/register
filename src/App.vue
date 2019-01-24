<template>
  <div id="app">
    <div class="container">
      <div class="row justify-content-center">
        <div class="col col-6">
          <div class="card">
            <h4 class="card-header bg-dark text-white">
              Register
            </h4>
          </div>
          <div class="card-body">
            <form action="">
              <div class="form-group">
                <label for="">User</label>
                <input
                        id="user_user"
                        v-model="user.user"
                        class="form-control"
                        type="text"
                        
                >
              </div>
              <div class="form-group">
                <label for="">Email</label>
                <input
                        id="user_email"
                        v-model="user.email"
                        class="form-control"
                        type="email">
              </div>
              <div class="form-group">
                <label for="">Password</label>
                <input
                        id="user_password"
                        v-model="user.password"
                        class="form-control"
                        type="password">
              </div>
              <div class="form-group">
                <label for="">Verjaardag</label>
                <input
                        id="user_verjaardag"
                        v-model="user.verjaardag"
                        class="form-control"
                        type="date">
              </div>
             
              <div class="form-group">
                <label for="">Biografie</label>
                <textarea
                        id="user.biografie"
                        v-model="user.biografie"
                        cols="30"
                        rows="10"
                        class="form-control">
                
                </textarea>
                
              </div>
              <div class="form-group">
                <label for="">Geslacht</label>
                <select class="form-control" v-model="user.geslacht">
                  <option
                          v-for="gender in genders"
                          :value="gender"
                          
                  >
                    {{ gender }}
                  </option>
                </select>
  
              </div>
              <div class="form-group">
               <div class="form-check">
                 <label for="" class="form-check-label">
                   <input
                           v-model="user.receiveNieuwsbrief"
                           type="checkbox"
                           class="form-check-input">
                   Nieuwsbrief?
                 </label>
               </div>
              </div>
              <div class="form-group">
                <button class="btn btn-primary">
                  Register
                </button>
                <button
                        @click="reset"
                        class="btn btn-danger">
                  Reset
                </button>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>


export default {
  name: 'app',
    
    data(){
      return{
          user:{
              user: '',
              email: '',
              password: '',
              verjaardag:'',
              biografie:'',
              geslacht:'',
              receiveNieuwsbrief:true
          },
          genders:[
              'man',
              'vrouw',
              'ietsanders'
          ]
      }
    },
    methods:{
      reset(){
          this.user = {
              user: '',
              email: '',
              password: '',
              verjaardag:'',
              biografie:'',
              geslacht:'',
              receiveNieuwsbrief:true
          }
      },
        register(){
        
        }
    }
    

}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
