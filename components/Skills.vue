<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>Skills</h1>
      </v-col>
    </v-row>
    <v-row v-for="skillGroup in skillGroups" :key="skillGroup.group">
      <v-col>
        <h4>
          {{ skillGroup.group.toUpperCase() }}
        </h4>
        {{ skillGroup.skills.join(', ') }}
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      skillGroups: [
        {
          group: 'languages',
          skills: ['python', 'typescript', 'SCL/STL/LAD', 'C#']
        },
        {
          group: 'frameworks',
          skills: ['flask', 'vue', '.NET', 'ASP.NET', 'express', 'pytest', 'mocha']
        },
        {
          group: 'Courses',
          skills: [
            'Basics of Programming (BMEVIEEAA00)',
            'Introduction to python and NLP (BMEVIAUAV35)',
            'Machine Learning with Python-From Linear Models to Deep Learning (MITx - 6.86x; audit course)'
          ]
        },
        {
          group: 'Operating systems',
          skills: ['Linux (Hash Linux, Ubuntu)', 'Windows 7-10']
        },
        {
          group: 'Languages',
          skills: ['English', 'Hungarian']
        },
        {
          group: 'Other',
          skills: ['Siemens TIA Portal',
            'docker',
            'git/gitlab/github',
            'Rest API',
            'test driven development',
            'domain driven development'
          ]
        }
      ]
    }
  }
}
</script>
