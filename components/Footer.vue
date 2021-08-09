<template>
    <div class="footer hero is-fullheight">
        <div class="contact">
            <form @submit.prevent="">
                <p class="get has-text-centered is-size-3 has-text-weight-bold has-text-black">Get in touch</p>
                <div class="field">
                    <div class="label">Name</div>
                    <div class="control">
                        <input class="input" type="text" v-model="name"/>
                    </div>
                </div>
                <div class="field">
                    <div class="label">Email</div>
                    <div class="control">
                        <input class="input" type="email" v-model="email"/>
                    </div>
                </div>
                <div class="field">
                    <div class="label">Message</div>
                    <div class="control">
                        <textarea class="textarea" v-model="message" ></textarea>
                    </div>
                </div>
                <button class="button is-fullwidth is-rounded" type="submit">Send</button>
                <div class="is-size-1 has-text-centered">
                    <ul>
                        <a href="https://github.com/SoyTanMax">
                            <li><i class="fab fa-github"></i></li>
                        </a>
                    </ul>
                </div>
            </form>
            <p class="logo is-uppercase has-text-centered">
                <strong>Max</strong>lópez
            </p>
            <p class="has-text-centered is-size-7">UI / UX Designer + Frontend Developer</p>
        </div>
    </div>
</template>

<script>
export default {
  name: 'Footer',
  data(){
      return{
        name: this.name,
        email: this.email,
        message: this.message
      }
  },
  head() {
      return{
          script: [
            {src:'https://use.fontawesome.com/releases/v5.3.1/js/all.js'}
        ]
    }
  },
  methods: {
      
  }
}
</script>

<style scoped>
    .footer{
        background: hsl(210, 38%,95%);
        font-family: 'Nunito', sans-serif;
    }
    form{
        max-width: 550px;
        margin: 0 auto;
    }
    .label{
        margin-bottom: 4px;
        font-size: 14px;
        color: hsl(210, 10%,38%)
    }
    .input{
        border-radius: 8px;
        box-shadow: none;
        background: white;
        padding: 8px;
    }
    .textarea{
        border-radius: 8px;
        box-shadow: none;
        background: white;
    }
    .button{
        border: none;
        color: white;
        background: linear-gradient(90deg, #26AED9 -9.85%, #3173B4 116.29%);
        padding: 12px 0px;
        margin: 24px 0px;
    }
    .get{
        font-weight: bold;
        font-size: 24px;
        line-height: 33px;
        color: hsl(0,0%, 20%);
        margin-bottom: 42px;
    }
    ul {
        display: flex;
        justify-content: space-evenly;
        margin-bottom: 32px;
    }
    li {
        color: #3173B4;
    }
    .logo{
        font-size: 20px;
    }
    @media screen and (max-width: 769px) {
        .hero{
            padding: 48px 24px 0 24px;
        }
    }
</style>