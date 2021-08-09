<template>
    <div class="tucausa">
        <img class="banner" :src="banner" alt="">
        <div class="header">
            <p class="is-size-3 has-text-weight-bold">Tu Causa</p>
            <a href="https://tucausa.netlify.app/">See live code</a>
        </div>
        <p class="is-size-5 has-text-justified has-text-weight-medium spacing">A social service UX/UI + Web development project.</p>
        <p class="is-size-5 has-text-weight-bold">About Tu Causa and some context</p>
        <p class="is-size-6 has-text-justified spacing">Tu Causa is meant to be a web platform where students from my university could enroll themselves in social service projects where they could either help with volunteering or donations.
            <br>At the university I belong to, it is necessary to perform a certain amount of hours of social service, for that reason I signed up for Thunder, a project where we help non-governmental organizations with their web pages. Tu Causa is was one of the projects I participated in. 
            At first, it was a complex situation because the project managers weren't sure what they wanted to build, so I had to figure it out by myself according to their needs (and by redesigning several times). <br>After several iterations, I concluded that they needed a Content Management System (CMS) since the ones that would be posting the projects on the platform would not be the site's admin but be the project managers of the non-governmental organizations. 
            <br> <strong>Note: </strong>Tu Causa means "your cause" in spanish, and it is just a temporary name we gave to the project to identify it since the ones proposed before were too large or not catchy at all.</p>
        
        <p class="is-size-5 has-text-weight-bold">User profiles</p>
        <p class="is-size-6 has-text-justified spacing">Basically, there were 3 main user profiles that will use the platform: </p>
        <li>Students: people interested in enrolling themselves on a social service project.</li>
        <li>Project managers of the non-governmental organizations: people interested in posting and recruiting help for their project.</li>
        <li class="spacing">Administrators: people in charge of managing the content posted in the site. </li>

        <p class="is-size-5 has-text-weight-bold">Platform's requirements</p>
        <p class="is-size-6 has-text-justified spacing">In general, the students, or common users, should be able to: </p>
        <li>See all the projects posted by the non-governamental organizations.</li>
        <li>Search projects through filters according to their preferences.</li>
        <li>See the projects details and contact the project managers. </li>
        <br>

        <p class="is-size-6 has-text-justified spacing">Project managers using this platform should be able to: </p>
        <li>Register an account for their organization through a form that would be checked later on by the admins. </li>
        <li>Post, edit and erase posts for their social service projects.</li>
        <li>Upload images for their posts.</li>
        <br>

        <p class="is-size-6 has-text-justified spacing">Admins should be able to: </p>
        <li>Review the forms from the organizations registered to post their projects.</li>
        <li>Control which projects get posted.</li>
        <br>
        
        <p class="is-size-5 has-text-weight-bold">{{"The site's architecture & User flow"}}</p>
        <p class="is-size-6 has-text-justified spacing">Since it was a project that needed a fast development, I didn't had a lot of time to design the wireframes properly, so I just drew the basic structure of the site and proceeded to make the final designs. <br> 
        The general idea is to build a site where you could see through the projects right away and filter them, so the home page is built to accomplish these task. After the hero section, I immediately placed the filters so the users can search whatever kind of project they're looking for. <br>
        Once you click on a specific project, you should be sent to that project page. Afterwards you can click on "see more" to get more information about the organization that posted that project or more projects related.
        </p>
        <div class="wireframes">
            <img class="image spacing" :src="image2" alt="">
            <p class="is-size-6 has-text-justified spacing">These sections below are meant to be used by the project managers of the organizations to manage the projects that they have posted.</p>
            <img class="image spacing" :src="image3" alt="">
        </div>

        <p class="is-size-5 has-text-weight-bold">Final designs</p>
        
        <p class="is-size-6 has-text-justified spacing">Home page</p>
        <img class="image spacing" :src="image4" alt="">
        
        <p class="is-size-6 has-text-justified spacing">Single product page</p>
        <img class="image spacing" :src="image5" alt="">
        
        <p class="is-size-6 has-text-justified spacing">Single organization page</p>
        <img class="image spacing" :src="image6" alt="">
        
        <p class="is-size-6 has-text-justified spacing">My projects</p>
        <img class="image spacing" :src="image7" alt="">
        
        <p class="is-size-6 has-text-justified spacing">Edit / create project</p>
        <img class="image spacing" :src="image8" alt="">
        
        <p class="is-size-6 has-text-justified spacing">Login page</p>
        <img class="image spacing" :src="image9" alt="">
        
        <p class="is-size-6 has-text-justified spacing">Register form</p>
        <img class="image spacing" :src="image10" alt="">
        
        <p class="is-size-5 has-text-weight-bold">UI elements</p><br>
        <img class="image spacing" :src="image11" alt="">

        <p class="is-size-5 has-text-weight-bold">Building the site</p>
        <p class="is-size-6 has-text-justified spacing">Once I had the designs ready, building the front end was going to be way easier. For this platform I decided to use Vue.js as the Javascript framework and Nuxt.js on top of it for a faster development. Additionally, Firebase was used in order to handle the authentication needed, the collections for the posts and the storage for the images in each post. <br> 
        Here is the link to <a href="https://tucausa.netlify.app/">see the live code</a> and the <a href="https://github.com/SoyTanMax/tucausa">github repository</a>.</p>
    </div>
</template>

<script>
    export default {
        layout: "normal",
        head(){
            return {
            title: "Freelance UX/UI Designer and Frontend Web Developer"
            }
        },
        data() {
            return {
                banner: require('~/assets/banner2.svg'),
                image1: require('~/assets/architecture.png'),
                image2: require('~/assets/image10.png'),
                image3: require('~/assets/image11.png'),
                image4: require('~/assets/image12.png'),
                image5: require('~/assets/image13.png'),
                image6: require('~/assets/image14.png'),
                image7: require('~/assets/image15.png'),
                image8: require('~/assets/image16.png'),
                image9: require('~/assets/image17.png'),
                image10: require('~/assets/image18.png'),
                image11: require('~/assets/image19.png'),
                slider: "Originally, I proposed a simple hero page with a heading, an image, and a call-to-action button, but the client suggested a slider with the main actions that you can take in the platform and I thought it was a great idea so we went with it. The slider consisted in two slides, one for buying and the other one for selling art. These slides were meant to contain custom graphics for Taconomics, graphics which we will see later on the Style Guide section.",
                artist: "These component is meant to change state when hovered on to see a description of the artist and a link to see its collection in full detail.",
                item:"These are meant to be card-like components to show an overview of the NFTs in the gallery, including its price, rarity, and a link to see its full detail.",
                buy: "The client and I decided to put these components together in the same page because they are very related talking about functionality, because without $TACO and $Salsa you can not buy art on the platform. In order to change from one component to another smoothly I suggested a switch view.",
                buy2:"The first component consists in a simple swap component that you can find in most of the cryptocurrency sites where you can buy of swap cryptos.",
                buy3:"The second component is a little bit more complex, given that there are two ways in which you can make Salsa: the multi-asset or the single-asset way. In the first one, you use $TACO and WETH to create $Salsa, and in the second one you select either $TACO or WETH to make $SALSA.",
                buy4:"To select either the multi-asset or the single asset way I suggested a select button so as not to spam the switch component. Once you select the multi-asset way, you have to choose again between $TACO and WETH, so I went with option buttons but designed in a way that doesn't feel like an option button.",
                style: "Since the begging the client mentioned that Taconomics needed a logo and a little bit of branding and I was delighted to work on it. At first, I suggested going with a 3d-like concept that has become very popular since last year but the client said he had a more of a flat style in mind.",
            }
        },
    }
</script>

<style scoped>
.header{
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
.tucausa{
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-left: 15%;
    margin-right: 15%;
    font-family: 'Nunito', sans-serif;
    margin-bottom: 24px;
}
.banner{
    max-height: 250px;
    margin: 20px 0;
}
.titulo{
    margin-top: 24px;
}
.spacing{
    margin-bottom: 24px;
}
.image{
    width: 100%;
    border-radius: 12px;
}
    @media screen and (max-width: 769px) {
        .tucausa{
            margin: 0 24px;
        }
        .banner{
            width: 100%;
        }
        .spacing{
            margin-bottom: 20px;
        }
        .header{
            display: flex;
            align-items: center;
            justify-content: space-between;
        }
        .image{
            width: 100%;
            border-radius: 8px;
        }
        .wireframes{
            display: flex;
            flex-direction: column;
        }
    }
</style>