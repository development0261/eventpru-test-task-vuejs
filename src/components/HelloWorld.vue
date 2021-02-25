<template>
    <div>
    <div :class="drawer ? 'overlay-css' : '' "></div>
    <v-system-bar class="mt-5 menubar">
        <div class="row mt-5">
            <div class="col-md-2">
               <img src="../assets/Frame1.png" class="img-class cursou-pointer">
            </div>

            <div class="col-md-8 icon-css">
                <v-text-field append-icon="search" placeholder="Vendors, products, packages, e-invitations and more...">
                </v-text-field>
            </div>

            <div class="col-md-2 icon-css">
                <div class="row">
                    <div class="col-4 cursou-pointer">
                        <img src="../assets/Group3614.png">
                    </div>
                    <div class="col-4 cursou-pointer">
                        <img src="../assets/Group3615.png">
                    </div>
                    <div class="col-4 cursou-pointer">
                        <img src="../assets/Group3616.png">
                    </div>
                </div>
            </div>
        </div>
    </v-system-bar>
    <!--left side bar-->
    <div class="main-wrap">
        <div class="sidebar-box">
            <v-app-bar color="deep-purple" dark class="app-css">
                <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
            </v-app-bar>
            <v-navigation-drawer v-model="drawer" absolute temporary class="app-css">
                  <v-list
                    nav
                    dense
                  >
                    <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
                        <v-list>
                    <v-list>
                      <v-list-item class="px-2">
                        <v-list-item-avatar>
                          <img src="../assets/Frame23.png" class="plus-sign">
                        </v-list-item-avatar>
                      </v-list-item>
                    </v-list>

                 <v-list nav dense>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame30.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame32.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame33.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame34.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                </v-list>
                </v-list>
                <v-list class="custom-icon">
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Vector.png"  class="blube-css">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>

                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/bx_bx-support.png" class="blube-css">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>

                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Group3610.png" class="blube-css">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                </v-list>
                    </v-list-item-group>
                  </v-list>
            </v-navigation-drawer>


            <!--desktop-->
             <v-navigation-drawer
                permanent
                class="mt-5 desktop-css">
                <v-list>
                    <v-list>
                      <v-list-item class="px-2">
                        <v-list-item-avatar>
                          <img src="../assets/Frame23.png" > 
                        </v-list-item-avatar>
                      </v-list-item>
                    </v-list>

                 <v-list nav dense>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame30.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame32.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame33.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Frame34.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                </v-list>
                </v-list>
                <v-list class="custom-icon">
                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Vector.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>

                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/bx_bx-support.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>

                  <v-list-item link>
                    <v-list-item-icon>
                      <img src="../assets/Group3610.png">
                    </v-list-item-icon>
                    <div class="bulets-css"></div>
                  </v-list-item>
                </v-list>
                
            </v-navigation-drawer>
        </div>
        <div class="container" style="margin-right: 40px;">
            <div class="row">
                <div class="col-12">
                    <div class="dropdown-wrap">
                        <v-select
                          :items="items"
                          label="Birthday"
                        ></v-select>                    
                        <v-select
                          :items="items"
                          label="Wedding"
                        ></v-select>                    
                        <v-select
                          :items="items"
                          label="Festive"
                        ></v-select>  
                        <v-select
                          :items="items"
                          label="Seasonal"
                        ></v-select>                    
                        <v-select
                          :items="items"
                          label="Anniversary"
                        ></v-select>                    
                        <v-select
                          :items="items"
                          label="Baby Shower"
                        ></v-select>  
                        <!-- <a href="#" class="design-own-btn">Design your own</a> -->
                        <v-btn depressed color="error" class="danger-btn">Design your own</v-btn>      
                    </div>        
                </div>
            </div>
            <div class="row">
                <div class="col-md-2 sub-side-bar">
                    <v-list class="list-group-class">
                        <v-list-group
                            v-for="item in listgroup"
                            :key="item.title"
                            v-model="item.active"
                            :prepend-icon="item.action"
                            no-action
                          >
                            <template v-slot:activator>
                              <v-list-item-content>
                                <v-list-item-title v-text="item.title"></v-list-item-title>
                              </v-list-item-content>
                            </template>

                            <v-list-item
                              v-for="child in item.items"
                              :key="child.title"
                            >
                              <v-list-item-content>
                                <v-list-item-title v-text="child.title"></v-list-item-title>
                              </v-list-item-content>
                            </v-list-item>
                          </v-list-group>
                    </v-list>
                </div>

                <div class="col-md-10 row">
                    <!-- <div class="col-md-3">
                        <v-select
                          :items="items"
                          label="Colors"
                        ></v-select>
                    </div>
                
                    <div class="col-md-3">
                        <v-select
                          :items="items"
                          label="Colors"
                        ></v-select>
                    </div> -->
                
                    <v-checkbox v-model="selected" label="Free" value="Free">Free</v-checkbox>
                    <v-checkbox v-model="selected" label="Premium" value="Premium">Premium</v-checkbox>
                    <v-checkbox v-model="selected" label="Static" value="Static">Static</v-checkbox>
                    <v-checkbox v-model="selected" label="Animated" value="Animated">Animated</v-checkbox>

                    <div class="col-md-3">
                        <v-select
                          :items="items"
                          label="Colors"
                        ></v-select>
                    </div>
                    <div class="row">
                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image32.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image16.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image48.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image43.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image39.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image37.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image38.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image35.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="row">
                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image33.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image31.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image34.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>

                        <div class="col-md-3">
                            <div
                                class="mx-auto my-12"
                                max-width="374"
                              >
                                <template slot="progress">
                                  <v-progress-linear
                                    color="deep-purple"
                                    height="10"
                                    indeterminate
                                  ></v-progress-linear>
                                </template>
                                <img src="../assets/image40.png" height="250" class="grid_img_box">
                                <div class="box-detail">
                                    <div class="bd-left">
                                        <p class="text-class">Cafe Badilico</p>
                                        <img src="../assets/Group3868.png" height="25" width="30" class="img-class-heart">
                                    </div>
                                    <div class="bd-right">
                                        <p class="text-class">Birthday</p>
                                        <span>Jon S</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                </div>

            </div>
        </div>
    </div>
</div>    
</template>
<script>
  export default {
    data() {
        return {
            items: ['Foo', 'Bar', 'Fizz', 'Buzz'],
            selected: ["Free"],
            selected: ["Premium"],
            selected: ["Static"],
            selected: ["Animated"],

             selectedItem: 0,
              demo: [
                { text: 'My Files' },
                { text: 'Shared with me' },
                { text: 'Starred' },
                { text: 'Recent' },
                { text: 'Offline' },
                { text: 'Uploads' },
                { text: 'Backups' },
              ],

               drawer: false,
                group: null,

              listgroup: [
                {
                  items: [{ title: 'List Item' }],
                  title: 'Sort',
                },
                {
                  
                  items: [
                    { title: 'Breakfast & brunch' },
                    { title: 'New American' },
                    { title: 'Sushi' },
                  ],
                  title: 'Filter By',
                },
                {
                  items: [{ title: 'List Item' }],
                  title: 'Event',
                },
                {
                  items: [{ title: 'List Item' }],
                  title: 'Theme',
                },
                {
                  items: [{ title: 'List Item' }],
                  title: 'Colours',
                },
                {
                  items: [{ title: 'List Item' }],
                  title: 'Designer',
                },
                {
                  items: [{ title: 'List Item' }],
                  title: 'Animation options',
                },
                {
                  items: [{ title: 'List Item' }],
                  title: 'Pricing',
                },
              ],
        };


  },
   
  }
</script>

