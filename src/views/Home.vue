<template>
<v-app id="home">
<NavBar />
<body>
  <v-container fluid>
      <v-row>
        <v-col cols="6">
          <v-img src="logo3.png" contain max-height="500"></v-img>
         </v-col>
        <v-col cols="6">
          <h5 class="red--text text-darken-4 top">Hello Im HammerX</h5>
          <h1 class="white--text">Software Engineer</h1>
          <p class="grey--text">
            the branch of computer science that deals with the design<br /> 
            development, testing, and maintenance of 
            <br /> software applications.
          </p>
          <v-btn tile color="#A7121D" dark>about me</v-btn>
        </v-col>
        <v-col cols="12" class="padd">  <br/> <br/> <br/> <br/> <br/>  <br/>
          <div class="first" id="project">
            <v-row>
              <v-col cols="12" >
                <div class="child bgcolor1">
                  <v-icon color="#A7121D" x-large class="ml-3">
                    mdi-palette-swatch
                  </v-icon>
                  <h3 class="white--text ml-3 mt-4">UI Design</h3>
                  <p class="grey--text ml-3 mt-6">
                    the branch of computer science <br />  that deals with the design
                    <br /> 
                          development, testing
                  </p>
                  <v-btn color="#A7121D" dark text>
                    know more
                    <v-icon right>mdi-arrow-right</v-icon>
                  </v-btn>
                </div>
                <div class="child bgcolor2">
                  <v-icon x-large class="ml-3" dark>mdi-shopping</v-icon>
                  <h3 class="white--text ml-3 mt-4">Product Design</h3>
                  <p class="grey--text ml-3 mt-6">
                    the branch of computer science <br />  that deals with the design
                    <br /> 
                          development, testing
                  </p>
                  <v-btn dark text>
                    know more
                    <v-icon right>mdi-arrow-right</v-icon>
                  </v-btn>
                </div>
                <div class="child bgcolor1">
                  <v-icon color="#A7121D" x-large class="ml-3">mdi-book-open-page-variant</v-icon>
                  <h3 class="white--text ml-3 mt-4">Branding</h3>
                  <p class="grey--text ml3 mt-6">
                    the branch of computer science <br />  that deals with the design
                    <br /> 
                     development, testing
                  </p>
                  <v-btn color="#A7121D" dark text>
                    know more
                    <v-icon right>mdi-arrow-right</v-icon>
                  </v-btn>
                </div> 
              </v-col>
              
              <v-col cols="12" class="mt-10"> <br/> <br/>
                  <v-row>
                    <v-spacer/>
                  <div class="child1">
                  <h1 class="red--text text-darken-4 mt-4 number">12</h1>
                  <h3 class="white--text mt-4">Years Experince</h3>
                 </div>
                 <div class="child2 mRight">
                  <v-row>
                    <v-col cols="12" class="childcol">
                      <div class="child2 mButton padding bgcolor1">
                        <h1 class="red--text text--darken-4">60+</h1>
                        <p class="grey--text">Clients</p>
                      </div>
                    </v-col>
                    <v-col cols="12" class="childcol">
                      <div class="child2  padding  bgcolor1">
                        <h1 class="red--text text--darken-4">122+</h1>
                        <p class="grey--text">Completed Project</p>
                      </div>
                    </v-col>
                 </v-row>
                 </div>
                 <div class="child2 ">
                  <v-row>
                    <v-col cols="12" class="childcol">
                      <div class="child2 mButton padding bgcolor1">
                        <h1 class="red--text text--darken-4">08</h1>
                        <p class="grey--text">Years Experience</p>
                      </div>
                    </v-col>
                    <v-col cols="12" class="childcol">
                      <div class="child2  padding bgcolor1">
                        <h1 class="red--text text--darken-4">10</h1>
                        <p class="grey--text">Achievements</p>
                      </div>
                    </v-col>
                  </v-row>
                 </div>
                 <v-spacer/>
                </v-row>
               
              </v-col>
            </v-row>
          </div>
        </v-col>
        <v-col md="3" offset-md="3" id="about">
          <h4 class="white--text">FEATURED PROJECTS</h4>
          <p class="grey--text">LOREM ipsum dolar Lorem ipsum dolar</p>
        </v-col>
        <v-col md="3" class="text-end">
          <v-btn title color="#A7121D" dark>View All</v-btn>
        </v-col>
        <v-col md="3" offset-md="3">
          <v-card class="pa-6 py-0" outlined tile height="300px"  color="#1E1E1E">
           <v-img src="logo3.png" contain></v-img>
          </v-card>
        </v-col>
         <v-col md="3">
          <v-card class="pa-6 py-0" outlined tile height="300px" color="#1E1E1E">
           <v-img src="logo3.png" contain ></v-img>
          </v-card>
         </v-col>
         <v-col md="3" offset-md="3">
          <v-btn color="white" dark text class="ml-n4">
            The Vintage
          </v-btn><br />
         
          <v-dialog
      v-model="dialog"
      width="800"
    >
      <template v-slot:activator="{ props }">
        <v-btn
        color="#A7121D" dark text class="ml-n4"
          v-bind="props"
        >
        know more
        <v-icon right>mdi-arrow-right</v-icon>
        </v-btn>
      </template>
      <v-card>
        <v-card-title>
          <span class="text-h5">Use Google's location service?</span>
        </v-card-title>
        <v-card-text>
          Lorem ipsum dolor sit amet, semper quis, sapien id natoque elit. Nostra urna at, magna at neque sed sed ante imperdiet, dolor mauris cursus velit, velit non, sem nec. Volutpat sem ridiculus placerat leo, augue in, duis erat proin condimentum in a eget, sed fermentum sed vestibulum varius ac, vestibulum volutpat orci ut elit eget tortor. Ultrices nascetur nulla gravida ante arcu. Pharetra rhoncus morbi ipsum, nunc tempor debitis, ipsum pellentesque, vitae id quam ut mauris dui tempor, aptent non. Quisque turpis. Phasellus quis lectus luctus orci eget rhoncus. Amet donec vestibulum mattis commodo, nulla aliquet, nibh praesent, elementum nulla. Sit lacus pharetra tempus magna neque pellentesque, nulla vel erat.
          Justo ex quisque nulla accusamus venenatis, sed quis. Nibh phasellus gravida metus in, fusce aenean ut erat commodo eros. Ut turpis, dui integer, nonummy pede placeat nec in sit leo. Faucibus porttitor illo taciti odio, amet viverra scelerisque quis quis et tortor, curabitur morbi a. Enim tempor at, rutrum elit condimentum, amet rutrum vitae tempor torquent nunc. Praesent vestibulum integer maxime felis. Neque aenean quia vitae nostra, tempus elit enim id dui, at egestas pulvinar. Integer libero vestibulum, quis blandit scelerisque mattis fermentum nulla, tortor donec vestibulum dolor amet eget, elit nullam. Aliquam leo phasellus aliquam curabitur metus a, nulla justo mattis duis interdum vel, mollis vitae et id, vestibulum erat ridiculus sit pulvinar justo sed. Vehicula convallis, et nulla wisi, amet vestibulum risus, quam ac egestas.
          Et vitae, nulla gravida erat scelerisque nullam nunc pellentesque, a dictumst cras augue, purus imperdiet non. Varius montes cursus varius vel tortor, nec leo a qui, magni cras, velit vel consectetuer lobortis vel. Nibh erat et wisi felis leo porttitor, sapien nibh sapien pede mi, sed eget porttitor, repellendus arcu ac quis. Luctus vulputate aut est sem magna, placerat accumsan nunc vestibulum ipsum ac auctor, maecenas lorem in ut nec mauris tortor, doloribus varius sem tortor vestibulum mollis, eleifend tortor felis tempus lacus eu eu. Eleifend vel eu, nullam maecenas mauris nec nunc euismod, tortor porta ridiculus potenti, massa tristique nam magna, et wisi placerat et erat ante. Eget pede erat in facilisis, fermentum venenatis sodales. Ac tortor sociis et non animi tristique, rhoncus malesuada, ut arcu volutpat scelerisque sollicitudin, elit curabitur dui pede purus dolor, integer aenean risus taciti nulla eleifend accumsan. At pulvinar diam parturient, interdum mi velit aliquet et a. Arcu at ac placerat eget justo semper, purus sociis curabitur mi ipsum consequat ut, mollis vestibulum, est ante ornare lacus sem. Neque magna mauris, commodo quisque, praesent semper suscipit lobortis nam. Justo malesuada cursus ac nunc litora nunc. Tellus ac, in lobortis nunc, montes lectus purus fermentum.
          Ac sit wisi. Sodales aliquam, sed vestibulum nullam arcu sit risus arcu, id luctus vitae lorem nibh, integer nec nullam class cursus mi, purus arcu lectus. Vel ante suscipit volutpat potenti mattis sed, wisi eu placerat aliquam erat, lectus morbi lobortis at assumenda. Consequat neque purus ipsum voluptas odio, netus vestibulum ut nec, suspendisse pellentesque nec enim in. Wisi dictum sed semper a, ipsum erat tellus habitasse est, erat sem ornare, vitae quisque ultricies. Dui sed blandit. Tempor et faucibus justo sed luctus, nec vitae vitae. Nunc nibh pede, ipsum vestibulum aenean leo ante ultricies, nam cras quis sed penatibus amet. In mauris a. Integer metus mauris tortor, et rutrum vestibulum ultricies, ut phasellus in ullamcorper ut mollit, eu justo. Cursus pretium venenatis.
          Cras pellentesque vel sodales accumsan aenean. Feugiat metus sit nec in aliquet amet, porttitor pretium vulputate massa. Consequat ipsum luctus quisque adipiscing libero. Wisi sollicitudin. Eget vitae ac lobortis, lorem natoque vestibulum et, aliquet faucibus at morbi nibh, vel condimentum. Massa unde orci sed id sed, odio donec congue nec praesent amet. Hymenaeos velit lacus, quis vivamus libero tempus duis, eu nisi eu, ipsum at accumsan pede justo morbi donec, massa et libero sit risus neque tortor. Ut sed sed etiam hendrerit dapibus, quis metus suspendisse nibh.
          Fringilla tempor felis augue magna. Cum arcu a, id vitae. Pellentesque pharetra in cras sociis adipiscing est. Nibh nec mattis at maecenas, nisl orci aliquam nulla justo egestas venenatis, elementum duis vel porta eros, massa vitae, eligendi imperdiet amet. Nec neque luctus suscipit, justo sem praesent, ut nisl quisque, volutpat torquent wisi tellus aliquam reprehenderit, curabitur cras at quis massa porttitor mauris. Eros sed ultrices. Amet dignissim justo urna feugiat mauris litora, etiam accumsan, lobortis a orci suspendisse. Semper ac mauris, varius bibendum pretium, orci urna nunc ullamcorper auctor, saepe sem integer quam, at feugiat egestas duis. Urna ligula ante. Leo elementum nonummy. Sagittis mauris est in ipsum, nulla amet non justo, proin id potenti platea posuere sit ut, nunc sit erat bibendum. Nibh id auctor, ab nulla vivamus ultrices, posuere morbi nunc tellus gravida vivamus.
          Mauris nec, facilisi quam fermentum, ut mauris integer, orci tellus tempus diam ut in pellentesque. Wisi faucibus tempor et odio leo diam, eleifend quis integer curabitur sit scelerisque ac, mauris consequat luctus quam penatibus fringilla dis, vitae lacus in, est eu ac tempus. Consectetuer amet ipsum amet dui, sed blandit id sed. Tellus integer, dignissim id pede sodales quis, felis dolorem id mauris orci, orci tempus ut. Nullam hymenaeos. Curabitur in a, tortor ut praesent placerat tincidunt interdum, ac dignissim metus nonummy hendrerit wisi, etiam ut.
          Semper praesent integer fusce, tortor suspendisse, augue ligula orci ante asperiores ullamcorper. In sit per mi sed sed, mi vestibulum mus nam, morbi mauris neque vitae aliquam proin senectus. Ac amet arcu mollis ante congue elementum, inceptos eget optio quam pellentesque quis lobortis, sollicitudin sed vestibulum sollicitudin, lectus parturient nullam, leo orci ligula ultrices. At tincidunt enim, suspendisse est sit sem ac. Amet tellus molestie est purus magna augue, non etiam et in wisi id. Non commodo, metus lorem facilisi lobortis ac velit, montes neque sed risus consectetuer fringilla dolor. Quam justo et integer aliquam, cursus nulla enim orci, nam cursus adipiscing, integer torquent non, fringilla per maecenas. Libero ipsum sed tellus purus et. Duis molestie placerat erat donec ut. Dolor enim erat massa faucibus ultrices in, ante ultricies orci lacus, libero consectetuer mauris magna feugiat neque dapibus, donec pretium et. Aptent dui, aliquam et et amet nostra ligula.
          Augue curabitur duis dui volutpat, tempus sed ut pede donec. Interdum luctus, lectus nulla aenean elit, id sit magna, vulputate ultrices pellentesque vel id fermentum morbi. Tortor et. Adipiscing augue lorem cum non lacus, rutrum sodales laoreet duis tortor, modi placerat facilisis et malesuada eros ipsum, vehicula tempus. Ac vivamus amet non aliquam venenatis lectus, sociosqu adipiscing consequat nec arcu odio. Blandit orci nec nec, posuere in pretium, enim ut, consectetuer nullam urna, risus vel. Nullam odio vehicula massa sed, etiam sociis mauris, lacus ullamcorper, libero imperdiet non sodales placerat justo vehicula. Nec morbi imperdiet. Fermentum sem libero iaculis bibendum et eros, eget maecenas non nunc, ad pellentesque. Ut nec diam elementum interdum. Elementum vitae tellus lacus vitae, ipsum phasellus, corporis vehicula in ac sed massa vivamus, rutrum elit, ultricies metus volutpat.
          Semper wisi et, sollicitudin nunc vestibulum, cursus accumsan nunc pede tempus mi ipsum, ligula sed. Non condimentum ac dolor sit. Mollis eu aliquam, vel mattis mollis massa ut dolor ante, tempus lacinia arcu. Urna vestibulum lorem, nulla fermentum, iaculis ut congue ac vivamus. Nam libero orci, pulvinar nulla, enim pellentesque consectetuer leo, feugiat rhoncus rhoncus vel. Magna sociosqu donec, dictum cursus ullamcorper viverra. Ultricies quis orci lorem, suspendisse ut vestibulum integer, purus sed lorem pulvinar habitasse turpis.
          +
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="green-darken-1"
            variant="text"
            @click="dialog = false"
          >
            Disagree
          </v-btn>
          <v-btn
            color="green-darken-1"
            variant="text"
            @click="dialog = false"
          >
            Agree
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
         </v-col>
         <v-col md="3" >
          <v-btn color="white" dark text class="ml-n4">
            Foodasa
          </v-btn><br />
          <v-btn color="#A7121D" dark text class="ml-n4">
            know more
            <v-icon right>mdi-arrow-right</v-icon>
          </v-btn>
         </v-col>
         <v-col md="3" offset-md="3">
          <v-card class="pa-6 py-0" outlined tile height="300px" color="#1E1E1E">
           <v-img src="logo3.png" contain></v-img>
          </v-card>
        </v-col>
         <v-col md="3">
          <v-card class="pa-6 py-0" outlined tile height="300px" color="#1E1E1E">
           <v-img src="logo3.png" contain></v-img>
          </v-card>
         </v-col>
         <v-col md="3" offset-md="3">
          <v-btn color="white" dark text class="ml-n4">
            The Vintage
          </v-btn><br />
          <v-btn color="#A7121D" dark text class="ml-n4">
            know more
            <v-icon right>mdi-arrow-right</v-icon>
          </v-btn>
         </v-col>
         <v-col md="3" >
          <v-btn color="white" dark text class="ml-n4">
            Foodasa
          </v-btn><br />
          <v-btn color="#A7121D" dark text class="ml-n4">
            know more
            <v-icon right>mdi-arrow-right</v-icon>
          </v-btn>
         </v-col>
         <v-col cols="12" class="padd topInverse"> <br/>
          <div class="second">
            <div class="secondchild1" id="contact"> 
            <v-row> 
              <v-col cols="7">
                <h1 class="white--text">
                  Let's Work together on your next project
                </h1>
                <p class="grey--text">
                  Let's Work together on  your next project  Let's Work together on  your next project
                </p>
              </v-col> 
              <v-spacer />
              <v-col cols="5">
                <v-btn tile color="#A7121D" dark class="mt-16 ml-16">Contact</v-btn>
              </v-col>
            </v-row>
          </div>
          </div>
          <v-toolbar class="topTolbar" color="#111111" dark flat>
            <div style="position: absolute; margin-left: auto; margin-right: auto; left: 0; right: 0; text-align: center;">
              <v-btn text>Home</v-btn>
              <v-btn text>Project</v-btn>
              <v-btn text>About</v-btn>
              <v-btn text>Contact</v-btn>
            </div>
          </v-toolbar>
          
         </v-col> 
        </v-row>
      <!-- </v-row>
      <v-col>
       <v-row>
        <employee-form @add:employee="addEmployee"/>
       </v-row>
        <v-row>
        
         <v-col>
          <employee-table class="grey--text ml3 mt-6"
          :employees="employees"
          @delete:employee="deleteEmployee"
          @edit:employee="editEmployee" />
         </v-col>
        </v-row>

       </v-col>
       <v-col> -->

       <!-- </v-col> -->
    </v-container>
</body>
 <Footer/>
  </v-app>
 
</template>

<script>
// import EmployeeForm from '../components/EmployeeForm.vue';
// @ is an alias to /src


import NavBar from "../components/NavBar.vue";
// import EmployeeTable from '../components/EmployeeTable.vue';
import Footer from "../components/Footer.vue";

export default {
  name: "Home",
  components: {
    // EmployeeTable,
    // EmployeeForm,
    NavBar,
    Footer
   
    
},
  data(){
    return {
      dialog: false,
      // employees: [
      //   {
      //     id:1,
      //     name: 'hammer',
      //     email: 'hammer@gmail.com'
      //   },
      //   {
      //     id:2,
      //     name: 'hammer',
      //     email: 'hammer@gmail.com'
      //   },
      //   {
      //     id:3,
      //     name: 'hammer',
      //     email: 'hammer@gmail.com'
      //   },
      // ]
    }

  },
  // methods: {
  //   addEmployee(employee) {
  //     const lastId = 
  //     this.employees.length > 0 ? this.employees[this.employees.length - 1].id : 0;
  //     const id = lastId + 1;
  //     const newEmployee = {...employee, id};

  //     this.employees = [...this.employees, newEmployee]
  //     console.log(this.employees)
  //   },
  //   deleteEmployee(id) {
  //     this.employees = this.employees.filter(employee => employee.id !== id )
  //   },
  //   editEmployee(id, updateEmployee) {
  //     this.employees = this.employees.map(employee => employee.id === id ? updateEmployee : employee)
  //   }
  // }
};

</script>

<style scoped>

.top {
  margin-top: 180px;
}
.topInverse{
  margin-top: -250px;
}
.topTolbar{
  margin-top: 100px;
  text-align: center;
}

.first {
  width: 100%;
  height: 640px;
  background: linear-gradient(
    to right,
    #181818,
    #181818 50%,
    #111111 50%,
    #111111 50%,

  );
  text-align: center;
  padding: 2rem 2rem;

}

.second {
  width: 100%;
  height: 400px;
  background: #181818;
  text-align: center;
  padding: 2rem 1rem;
}

.secondchild1 {
  display: inline-block;
  background-color: #1e1e1e;
  padding: 2rem ;
  vertical-align: middle;
  text-align: left;
  margin-top: 250px;

}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: left;
  margin-right: 8px;
}

.bgcolor1 {
  background-color: #1e1e1e ;

}
.bgcolor2 {
  background-color: #ce1d2a ;

}

.child1 {
  display: inline-block ;
  padding: 2rem rem;
  vertical-align: middle;
  margin-right: 5px;
  width: 240px;
}

.child2 {
  display: inline-block0;
  width: 285px;
  vertical-align: middle;
}

.mRight {
  margin-right:8px;
}
.mButton{
  margin-bottom: 8px;
}
.padding{
  padding: 8px 0px;
}
.col-12.padd {
  padding :12px  !important;
}

.col-12.childcol {
  padding:0 !important;
}

h1.number {
  font-size: 60px;
  font-weight: bold;
}

body, html {
  padding: 0;
  margin: 0;
  width: 100%;
  min-height: 100%;
  
}
body {
  background-color: #111111;
}
</style>

