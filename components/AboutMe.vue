<template>
  <v-container>
    <v-row>
      <v-col>
        <h1> About me </h1>
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        Hi! I am <b>Bálint Hegedüs</b>, a chemical engineer in paper, a software developer at heart and
        a full-stack web application developer as described in my current job title. You can read about my
        journey on how did I get from learning chemical engineering to becoming a full-stack developer.
      </v-col>
    </v-row>
    <v-row>
      <v-col>
        <v-timeline :dense="$vuetify.breakpoint.xs">
          <v-timeline-item
            v-for="story in stories"
            :key="story.image"
            color="blue-grey darken-4"
          >
            <span slot="opposite"><img :src="story.image" width="150vmax"></span>
            <v-card>
              <v-card-text style="font-size: 16px">
                {{ story.text }}
              </v-card-text>
            </v-card>
          </v-timeline-item>
        </v-timeline>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      stories: [
        {
          text: `
          At 2013 I was faced with a huge decision. Do I want to follow my dreams in chemistry,
          or in information technology. At that time I decided to cast my vote with chemistry,
          and thus started studying chemical engineering at the Budapest University of Technology
          and Economics. While I enjoyed my time there, I could not stop the calling of software
          development, so at my final semester I took up a course in programming.
          `,
          image: '/university.svg'
        },
        {
          text: `
          During this time, as I had to decide on my master's, I again started thinking about changing my
          current field to something more related to IT, but due to personal reasons, I could not make
          that leap. But that does not deter me from chasing my dreams, I started to search for
          internship in an IT company. That is how I started working at SAP as an Application Support
          Intern. While this took me a step closer to my dreams, but I also came to realise, that
          I do not want to interact with software, I want to make one.
          `,
          image: '/support.svg'
        },
        {
          text: `
          To achieve my goals, I started to focus on my strengths as a chemical engineer, who loves
          to tinker around with code, and that is how I found my way to the world of PLCs and industrial
          autmation. As a chemical engineer I had domain knowledge (in the chemical industry), but
          I also possessed the ability to write code. Because of this, I started working for a small firm,
          who was a contractor for Egis Pharmaceutical Company. Here, I had the opportunity to plan, and
          develop software, which controlled the water purification and distribution process for a newly
          built plant. Also I wrote my master thesis at this company about indastrial automation and ISA-S88
          standard.
          `,
          image: '/industry.svg'
        },
        {
          text: `
          But my luck turned again and after finishing my master studies in June of 2019, it turned out, the firm
          I worked for unfortunately could not provide a full-time job for me. Because of this, I started looking for
          a job (related to industrial automation), and that is how I found my place at Evosoft Hungary as a
          Test Automation Engineer. I decided to accept this role, as I believed, that I will have the opportunity
          to gain deeper knowledge with PLCs (as my team was testing the Siemens TIA portal). This turned out to
          be true, but I also learned (once again) a more valuable lesson. That I do not want to use software but to
          make one. This is why my career here lasted not even a year, and I left in March of 2020.
          `,
          image: '/tester.svg'
        },
        {
          text: `
          Because of my disinterest in beeing a full-time test engineer, I started to help out my friends with a project at
          the autumn of 2019. This project was so successful for us, that we were able to switch from having this as
          a side project for us to becoming our full-time work! I continue to work for them as a contractor, and since
          the start of 2021 not just as a developer, but as the technical lead for the project.
          `,
          image: '/webpage.svg'
        }
      ]
    }
  }
}
</script>
