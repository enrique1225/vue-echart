
<template>
  <v-row class="portfolio-row">
    <div class="my-mobile-menu">
      <router-link to="/profile">
        <div
          class="moblie-logo-img"
          style="background:url(https://www.bavarealtors.in/wp-content/uploads/2019/11/dummy-man-570x570.png);"
        ></div>
      </router-link>
      <menu-component></menu-component>
    </div>
    <side-bar-component></side-bar-component>
    <v-col cols="8" class="portfolio-left">
      <v-col cols="12" md="12" class="input-img wa-prt-srch">
        <v-img src="../../assets/magnifying-glass.svg" class="prt-srch-logo"></v-img>
        <v-text-field label="Search" solo></v-text-field>
      </v-col>

      <v-row>
        <v-col cols="12" xs="12" class="text-right">
          <!-- <v-btn class="property-top-btns">
            <span></span> Portfolio
            <v-img src="../../assets/arrow-down.png"></v-img>
          </v-btn>-->

          <v-list id="dropdown-example" class="last-btns-p">
            <v-overflow-btn
              class="my-2"
              :items="properties"
              label="Portfolio"
              target="#dropdown-example"
            ></v-overflow-btn>
          </v-list>
        </v-col>
      </v-row>

      <chart-component />

      <v-col cols="3" class="portfolio-right profile-since only-mobile-show pd-bottom">
        <h4>97 Roslin Ave, Toronto, Ontario</h4>

        <v-list-item class="light-b-property">
          <v-list-item-action>
            <v-img src="../../assets/portfolio-p.png" class="list-img-g"></v-img>
          </v-list-item-action>
        </v-list-item>

        <v-card-actions class="v-padding">
          <v-btn class="drop-det-show" icon @click="show = !show">
            Details
            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show">
            <v-row class="padding-t">
              <v-col cols="6" xs="12" class>
                <v-card-text class="details-inlines">
                  <v-img src="../../assets/bed.svg" class="list-img-g"></v-img>5
                </v-card-text>
              </v-col>
              <v-col cols="6" xs="12" class="text-right">
                <v-card-text class="details-inlines">
                  <v-img src="../../assets/bathroom.svg" class="list-img-g"></v-img>4
                </v-card-text>
              </v-col>
              <v-col cols="6" xs="12" class>
                <v-card-text class="details-inlines">
                  <v-img src="../../assets/width.svg" class="list-img-g"></v-img>40 x 125
                </v-card-text>
              </v-col>
              <v-col cols="6" xs="12" class="text-right">
                <v-card-text class="details-inlines">
                  <v-img src="../../assets/tax(1).svg" class="list-img-g"></v-img>Mount Pleasant
                </v-card-text>
              </v-col>
            </v-row>
          </div>
        </v-expand-transition>

        <v-card-actions class="v-padding">
          <v-btn class="drop-det-show" icon @click="showHistory = !showHistory">
            Explore
            <v-icon>{{ showHistory ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="showHistory">
            <v-row class="explore-main">
              <v-col cols="3" xs="12" class>
                <v-card-text class="explore-inlines">
                  <v-img src="../../assets/calendar(1).svg"></v-img>2009
                </v-card-text>
              </v-col>
              <v-col cols="6" xs="12" class>
                <v-card-text class="explore-inlines">
                  <v-img class="explore-img-c" src="../../assets/coin(1).svg"></v-img>$21,00,000
                </v-card-text>
              </v-col>
              <v-col cols="3" xs="12" class="padding-l">
                <v-card-text class="explore-inlines">
                  <v-btn class="property-table-btns">Sold</v-btn>
                </v-card-text>
              </v-col>
            </v-row>
            <v-row class="explore-main">
              <v-col cols="3" xs="12" class>
                <v-card-text class="explore-inlines">
                  <v-img src="../../assets/calendar(1).svg"></v-img>2004
                </v-card-text>
              </v-col>
              <v-col cols="6" xs="12" class>
                <v-card-text class="explore-inlines">
                  <v-img class="explore-img-c" src="../../assets/coin(1).svg"></v-img>$1,300,000
                </v-card-text>
              </v-col>
              <v-col cols="3" xs="12" class="padding-l">
                <v-card-text class="explore-inlines">
                  <v-btn class="property-table-btns">Sold</v-btn>
                </v-card-text>
              </v-col>
            </v-row>
            <v-row class="explore-main">
              <v-col cols="4" xs="12" class="pd-left">
                <v-card-text class="explore-inlines">
                  <v-img class="calendar-img-c" src="../../assets/calendar(1).svg"></v-img>1999
                </v-card-text>
              </v-col>
              <v-col cols="5" xs="12" class></v-col>
              <v-col cols="3" xs="12" class="padding-l">
                <v-card-text class="explore-inlines btn-right-c">
                  <v-btn class="property-table-btns">Built</v-btn>
                </v-card-text>
              </v-col>
            </v-row>
            <v-card-text></v-card-text>
          </div>
        </v-expand-transition>
        <!-- <v-row class="explore-main">
          <v-col cols="12" xs="12" class="remove-propertys">
            <v-btn>Remove Property</v-btn>
          </v-col>
        </v-row>-->
      </v-col>

      <v-card class="property-cards-chart">
        <v-row>
          <v-col class="col-xs-12 col-md-6">
            <h4 class="mini-fix-heading">Alert</h4>
            <v-list class="portfolio-lists">
              <v-list-item>
                <v-list-item-content>
                  <v-img src="../../assets/growth.svg" class="list-img-g"></v-img>
                  <p>CREA has projected a positive outlook for this neighbourhood</p>
                </v-list-item-content>
              </v-list-item>
              <v-list-item>
                <v-list-item-content>
                  <v-img src="../../assets/open.svg" class="list-img-g"></v-img>
                  <p>65% of properties in the neighbourhoodhave sold over asking in the past 30 days.</p>
                </v-list-item-content>
              </v-list-item>
            </v-list>
          </v-col>
          <v-col class="col-xs-12 col-md-6">
            <h4 class="mini-fix-heading">Scores</h4>
            <v-list class="portfolio-lists scores-items-x">
              <v-row>
                <v-col class="col-xs-12 col-md-4">
                  <div class="progress" data-percentage="73">
                    <span class="progress-left">
                      <span class="progress-bar"></span>
                    </span>
                    <span class="progress-right">
                      <span class="progress-bar"></span>
                    </span>
                    <div class="progress-value">
                      <div>
                        <v-img src="../../assets/walk.svg" class="walk-imgs"></v-img>
                        <span>Walk Score</span>
                        <h1>73%</h1>
                      </div>
                    </div>
                  </div>
                </v-col>
                <v-col class="col-xs-12 col-md-4">
                  <div class="progress" data-percentage="43">
                    <span class="progress-left">
                      <span class="progress-bar"></span>
                    </span>
                    <span class="progress-right">
                      <span class="progress-bar"></span>
                    </span>
                    <div class="progress-value">
                      <div>
                        <v-img src="../../assets/box.svg"></v-img>
                        <span>Transit Score</span>
                        <h1>43%</h1>
                      </div>
                    </div>
                  </div>
                </v-col>
                <v-col class="col-xs-12 col-md-4">
                  <div class="progress" data-percentage="90">
                    <span class="progress-left">
                      <span class="progress-bar"></span>
                    </span>
                    <span class="progress-right">
                      <span class="progress-bar"></span>
                    </span>
                    <div class="progress-value">
                      <div>
                        <v-img src="../../assets/steering-wheel.svg"></v-img>
                        <span>Bike Score</span>
                        <h1>90%</h1>
                      </div>
                    </div>
                  </div>
                </v-col>
              </v-row>
            </v-list>
          </v-col>
        </v-row>
      </v-card>

      <v-card class="activity-table-prp">
        <v-row>
          <v-col cols="6" xs="12" class>
            <h4 class="mini-fix-heading">Activity</h4>
          </v-col>
          <v-col cols="6" xs="12" class="text-right">
            <h4 class="mini2-fix-heading">Period (30 Days)</h4>
          </v-col>
        </v-row>
        <v-simple-table>
          <template v-slot:default>
            <tbody>
              <tr v-for="item in desserts" :key="item.name">
                <td>{{ item.name }}</td>
                <td>
                  <v-img width="19" src="../../assets/money(2).svg" class="list-img-g"></v-img>
                  {{ item.price }}
                </td>
                <td>
                  <v-img width="15" src="../../assets/placeholder.svg" class="list-img-g"></v-img>
                  {{ item.distances }}
                </td>
                <td class="text-right">
                  <v-btn class="property-table-btns">Sold</v-btn>
                </td>
              </tr>
            </tbody>
          </template>
        </v-simple-table>
      </v-card>
    </v-col>
    <v-col cols="3" class="portfolio-right profile-since only-mobile-hide">
      <h4>97 Roslin Ave, Toronto, Ontario</h4>

      <v-list-item class="light-b-property">
        <v-list-item-action>
          <v-img src="../../assets/portfolio-p.png" class="list-img-g"></v-img>
        </v-list-item-action>
      </v-list-item>

      <v-card-actions class="v-padding">
        <v-btn class="drop-det-show" icon @click="show = !show">
          Details
          <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="show">
          <v-row class="padding-t">
            <v-col cols="6" xs="12" class>
              <v-card-text class="details-inlines">
                <v-img src="../../assets/bed.svg" class="list-img-g"></v-img>5
              </v-card-text>
            </v-col>
            <v-col cols="6" xs="12" class="text-right">
              <v-card-text class="details-inlines">
                <v-img src="../../assets/bathroom.svg" class="list-img-g"></v-img>4
              </v-card-text>
            </v-col>
            <v-col cols="6" xs="12" class>
              <v-card-text class="details-inlines">
                <v-img src="../../assets/width.svg" class="list-img-g"></v-img>40 x 125
              </v-card-text>
            </v-col>
            <v-col cols="6" xs="12" class="text-right">
              <v-card-text class="details-inlines">
                <v-img src="../../assets/tax(1).svg" class="list-img-g"></v-img>Mount Pleasant
              </v-card-text>
            </v-col>
          </v-row>
        </div>
      </v-expand-transition>

      <v-card-actions class="v-padding">
        <v-btn class="drop-det-show" icon @click="showHistory = !showHistory">
          Explore
          <v-icon>{{ showHistory ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
        </v-btn>
      </v-card-actions>

      <v-expand-transition>
        <div v-show="showHistory" class="pd-btm-20">
          <v-row class="explore-main">
            <v-col cols="3" xs="12" class>
              <v-card-text class="explore-inlines">
                <v-img src="../../assets/calendar(1).svg"></v-img>2009
              </v-card-text>
            </v-col>
            <v-col cols="6" xs="12" class>
              <v-card-text class="explore-inlines">
                <v-img class="explore-img-c" src="../../assets/coin(1).svg"></v-img>$21,00,000
              </v-card-text>
            </v-col>
            <v-col cols="3" xs="12" class="padding-l">
              <v-card-text class="explore-inlines">
                <v-btn class="property-table-btns">Sold</v-btn>
              </v-card-text>
            </v-col>
          </v-row>
          <v-row class="explore-main">
            <v-col cols="3" xs="12" class>
              <v-card-text class="explore-inlines">
                <v-img src="../../assets/calendar(1).svg"></v-img>2004
              </v-card-text>
            </v-col>
            <v-col cols="6" xs="12" class>
              <v-card-text class="explore-inlines">
                <v-img class="explore-img-c" src="../../assets/coin(1).svg"></v-img>$1,300,000
              </v-card-text>
            </v-col>
            <v-col cols="3" xs="12" class="padding-l">
              <v-card-text class="explore-inlines">
                <v-btn class="property-table-btns">Sold</v-btn>
              </v-card-text>
            </v-col>
          </v-row>
          <v-row class="explore-main">
            <v-col cols="4" xs="12" class="pd-left">
              <v-card-text class="explore-inlines">
                <v-img class="calendar-img-c" src="../../assets/calendar(1).svg"></v-img>1999
              </v-card-text>
            </v-col>
            <v-col cols="5" xs="12" class></v-col>
            <v-col cols="3" xs="12" class="padding-l">
              <v-card-text class="explore-inlines btn-right-c">
                <v-btn class="property-table-btns">Built</v-btn>
              </v-card-text>
            </v-col>
          </v-row>
        </div>
      </v-expand-transition>
      <v-row class="explore-main">
        <v-col cols="12" xs="12" class="remove-propertys text-center">
          <v-btn @click="removeProperties()">Remove Property</v-btn>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
import ChartComponent from "../../components/charts/ChartComponent";
import MenuComponent from "./../../components/Menu";
import SideBarComponent from "./../../components/SideBar";

export default {
  name: "Property",
  methods: {
    removeProperties: function () {
      // console.log('this.', this.$swal('Are you sure you want to remove this property?'))
      const resp = this.$swal({
        title: "Are you sure?",
        text: "Are you sure you want to remove this property?",
        icon: "warning",
        showCancelButton: true,
        confirmButtonText: "Yes, remove it!",
        cancelButtonText: "No, keep it",
      });
      resp.then(
        (result) => {
          console.log("result", result);
        },
        (error) => {
          console.log("error", error);
        }
      );
    },
  },
  data: () => ({
    show: true,
    showHistory: true,
    desserts: [
      {
        name: "55 Lawrence Ave E",
        price: "$1,995,000",
        distances: "1.7KM Away",
      },
      {
        name: "224 Lawrence Ave E",
        price: "$2,650,000",
        distances: "1.2KM Away",
      },
      {
        name: "34 Cranbrooke Ave",
        price: "$2,799,000",
        distances: "2.4KM Away",
      },
      {
        name: "9096 Range Street",
        price: "$5,430,382",
        distances: "5.2KM Away",
      },
      {
        name: "#2701 - 16 Yonge St",
        price: "$835,000",
        distances: "4.5KM Away",
      },
    ],
    properties: ["property 1", "property 2", "property 3", "property 4"],
  }),
  components: {
    ChartComponent,
    MenuComponent,
    SideBarComponent,
  },
};
</script>

<style scoped>
@import url("./property.scss");
</style>