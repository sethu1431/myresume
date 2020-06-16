<template>
  <div class="skillbar">
    <v-layout align-center justify-center wrap mt-3 pt-3 style="background:white">
      <v-flex xs12 md12 class="justify-center layout">
        <p class="heading">Skills</p>
      </v-flex>
      <v-flex xs12 md12>
        <v-layout align-center justify-center wrap>
          <v-flex xs12 md4 px-3>
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Html"
              :level="90"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Css"
              level="90"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Java script"
              level="70"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="vue js"
              level="85"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Social media Marketing"
              level="95"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Event Management"
              level="95"
            />
          </v-flex>
          <v-flex xs12 md4 px-3>
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px"
              class="my-5"
              fontColor="#fff"
              skill="React"
              level="40"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="React native"
              level="40"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="C Language"
              level="70"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Python"
              level="60"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Team Player"
              level="95"
            />
            <skill-bar
              barSize="15"
              barColor="#0E6FFA"
              bgcolor="#DCDCDC"
              style="border-radius:40px;border-color:#EEEEEE;border-style:solid;border-width:3px;"
              class="my-5"
              fontColor="#fff"
              skill="Digital marketing"
              level="85"
            />
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
import { SkillBar } from "vue-skill-bar";
export default {
  name: 'skillbar',
  components: {
    "skill-bar": SkillBar
  },
}
</script>