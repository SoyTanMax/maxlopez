<template>
    <div class="tucausa">
        <img class="banner" :src="banner" alt="">
        <div class="header">
            <p class="is-size-3 has-text-weight-bold">Tu Causa</p>
            <a href="https://tucausa.netlify.app/">See live code</a>
        </div>
        <p class="is-size-5 has-text-justified has-text-weight-medium spacing">A social service UX/UI + Web development project.</p>
        <p class="is-size-5 has-text-weight-bold">About Taconomics</p>
        <p class="is-size-6 has-text-justified spacing">{{about}}</p>
        <p class="is-size-5 has-text-weight-bold">Platform's requirements</p>
        <p class="is-size-6 has-text-justified spacing">{{requirements}}</p>
        <li>Explore and buy different digital art pieces.</li>
        <li>See the purchased pieces.</li>
        <li>Buy $TACO.</li>
        <li>Stake $Salsa (an alternative cryptocurrency used to buy unique art pieces) and obtain Lemons(the platform's main currency to buy art).</li>
        <li>Know more about the whole project and get information about the smart contracts. </li>
        <li>Communicate with the Taconomics team so people could enroll themselves as artists.</li>
        <br>
        <p class="is-size-6 has-text-justified spacing">But that was not everything, because the platform was needed to built for artists too, so they could: </p>
        <li>Create their collections.</li>
        <li>Post their art.</li>
        <li>And claim their earnings from the NFTs sold. </li>
        <br>
        <p class="is-size-5 has-text-weight-bold">User profiles</p>
        <p class="is-size-6 has-text-justified">With that being said, I could get the answer to a very important question: <strong>"Who are we building this site for?"</strong></p>
        <p class="is-size-6 has-text-justified spacing">Basically, there were 3 main user profiles that will use the platform: </p>
        <li>Collectors: people interested in buying digital art.</li>
        <li>Artists: people that want to publish and sell their art.</li>
        <li class="spacing">Administrators: people that have permissions to edit the site's content.</li>
        <p class="is-size-6 has-text-justified spacing">These types of users need to connect a wallet on the Ethereum network via Metamask to access all the functions of the platform. The last type of user is the one who is only "visiting" the platform and has permissions limited to read-only.</p>
        
        <p class="is-size-5 has-text-weight-bold">{{"The site's architecture & User flow"}}</p>
        <p class="is-size-6 has-text-justified spacing">{{architecture}}</p>
        <img class="image spacing" :src="image1" alt="">
        <p class="is-size-5 has-text-weight-bold">Wireframing</p>
        <div class="wireframes">
            <img class="image spacing" :src="image2" alt="">
            <img class="image spacing" :src="image3" alt="">
            <img class="image spacing" :src="image4" alt="">
            <img class="image spacing" :src="image5" alt="">
        </div>
        <p class="is-size-5 has-text-weight-bold">Main components</p>
        <p class="is-size-6 has-text-weight-bold">The slider</p>
        <p class="is-size-6 has-text-justified spacing">{{slider}}</p>
        <img class="image spacing" :src="image6" alt="">
        <p class="is-size-6 has-text-weight-bold">Artist component</p>
        <p class="is-size-6 has-text-justified spacing">{{artist}}</p>
        <img class="image spacing" :src="image7" alt="">
        <p class="is-size-6 has-text-weight-bold">Item component</p>
        <p class="is-size-6 has-text-justified spacing">{{item}}</p>
        <img class="image spacing" :src="image8" alt="">
        <p class="is-size-6 has-text-weight-bold">Buy Taco / Stake Salsa component</p>
        <p class="is-size-6 has-text-justified spacing">{{buy}}</p>
        <p class="is-size-6 has-text-justified spacing">{{buy2}}</p>
        <p class="is-size-6 has-text-justified spacing">{{buy3}}</p>
        <p class="is-size-6 has-text-justified spacing">{{buy4}}</p>
        <img class="image spacing" :src="image8" alt="">

        <p class="is-size-5 has-text-weight-bold">Style Guide</p>
        <p class="is-size-6 has-text-justified spacing">{{style}}</p>
        <p class="is-size-6 has-text-weight-bold">Choosing the typography</p>
        <p class="is-size-6 has-text-justified spacing">{{typo}}</p>
        <div class="columns">
            <div class="column">
                <img class="image spacing" :src="image9" alt="">
            </div>
            <div class="column">
                <p class="is-size-6 has-text-justified spacing">{{typo2}}</p>
            </div>
        </div>
        <p class="is-size-6 has-text-weight-bold">Designing the Logo</p>
        <p class="is-size-6 has-text-justified spacing">{{logo}}</p>
        <p class="is-size-6 has-text-justified spacing">{{logo2}}</p>
        <img class="image spacing" :src="image10" alt="">
        <p class="is-size-6 has-text-weight-bold">SVG Assets</p>
        <p class="is-size-6 has-text-justified spacing">{{assets}}</p>
        <img class="image spacing" :src="image11" alt="">
        <p class="is-size-6 has-text-weight-bold">Color Palette</p>
        <img class="image spacing" :src="image12" alt="">
        <p class="is-size-6 has-text-weight-bold">UI elements</p>
        <img class="image spacing" :src="image13" alt="">
        <p class="is-size-5 has-text-weight-bold">Final Designs</p>
        <p class="is-size-6 has-text-justified spacing">The slider</p>
        <img class="image spacing" :src="image14" alt="">
        <p class="is-size-6 has-text-justified spacing">Artist component</p>
        <img class="image spacing" :src="image15" alt="">
        <p class="is-size-6 has-text-justified spacing">Items component</p>
        <img class="image spacing" :src="image16" alt="">
        <p class="is-size-6 has-text-justified spacing">Buy item view</p>
        <img class="image spacing" :src="image17" alt="">
        <p class="is-size-6 has-text-justified spacing">Navigation bar active / Buy Taco / Stake Salsa component</p>
        <img class="image spacing" :src="image18" alt="">
        <p class="is-size-6 has-text-justified spacing">Sell your art</p>
        <img class="image spacing" :src="image19" alt="">
    </div>
</template>

<script>
    export default {
        layout: "normal",
        data() {
            return {
                banner: require('~/assets/banner2.svg'),
                image1: require('~/assets/architecture.png'),
                image2: require('~/assets/image.png'),
                image3: require('~/assets/image1.png'),
                image4: require('~/assets/image2.png'),
                image5: require('~/assets/image3.png'),
                image6: require('~/assets/slider.png'),
                image7: require('~/assets/artist.png'),
                image8: require('~/assets/item.png'),
                image8: require('~/assets/buy.png'),
                image9: require('~/assets/fonts.png'),
                image10: require('~/assets/logo.png'),
                image11: require('~/assets/assets.svg'),
                image12: require('~/assets/colors.png'),
                image13: require('~/assets/ui.png'),
                image14: require('~/assets/image4.png'),
                image15: require('~/assets/image5.png'),
                image16: require('~/assets/image6.png'),
                image17: require('~/assets/image7.png'),
                image18: require('~/assets/image8.png'),
                image19: require('~/assets/image9.png'),
                about: "Taconomics is meant to be a decentralized application (DApp) that seeks to create a launchpad so that latino artists can make themselves known through their digital art. In other words, it's an NFT art gallery where all the art exposed is in some way related to Tacos, because $TACO is the cryptocurrency used in this platform.",
                architecture: "Taking into account the different user types and the platform requirements, I came up with the platform's general user flow: ",
                requirements: "After talking to the client, who is the responsable and founder of Taconomics, I got a pretty good notion of what we needed to build. This notion arose from listing the requirements of the product, including its functional and non functional properties. Generally speaking, Taconomics needed to be a web application that allowed the user to:",
                slider: "Originally, I proposed a simple hero page with a heading, an image, and a call-to-action button, but the client suggested a slider with the main actions that you can take in the platform and I thought it was a great idea so we went with it. The slider consisted in two slides, one for buying and the other one for selling art. These slides were meant to contain custom graphics for Taconomics, graphics which we will see later on the Style Guide section.",
                artist: "These component is meant to change state when hovered on to see a description of the artist and a link to see its collection in full detail.",
                item:"These are meant to be card-like components to show an overview of the NFTs in the gallery, including its price, rarity, and a link to see its full detail.",
                buy: "The client and I decided to put these components together in the same page because they are very related talking about functionality, because without $TACO and $Salsa you can not buy art on the platform. In order to change from one component to another smoothly I suggested a switch view.",
                buy2:"The first component consists in a simple swap component that you can find in most of the cryptocurrency sites where you can buy of swap cryptos.",
                buy3:"The second component is a little bit more complex, given that there are two ways in which you can make Salsa: the multi-asset or the single-asset way. In the first one, you use $TACO and WETH to create $Salsa, and in the second one you select either $TACO or WETH to make $SALSA.",
                buy4:"To select either the multi-asset or the single asset way I suggested a select button so as not to spam the switch component. Once you select the multi-asset way, you have to choose again between $TACO and WETH, so I went with option buttons but designed in a way that doesn't feel like an option button.",
                style: "Since the begging the client mentioned that Taconomics needed a logo and a little bit of branding and I was delighted to work on it. At first, I suggested going with a 3d-like concept that has become very popular since last year but the client said he had a more of a flat style in mind.",
                typo: "For me the typography you use in a product is a very important aspect of the design (and should for every company) because it helps a ton to build the product's image. Since we were building something flat and not that serious, I suggested 5 different fonts for the client to choose (it could be one or two).",
                typo2: "Most of the designs contain Nunito and the Monserrat was used very subtly in some UI elements.",
                logo: "For some reason, I couldn't picture anything but a Taco with a smile, so I did my best to meet the client's requirements. The design is also very cohesive with the chosen typography.",
                logo2: "Fun fact / Note: In Mexico, it's very common to go to a Taco stand and when you are offered salsa, they put it in a bottle similar to the 'i' in Taconomics, that's why it looks like that. ",
                assets: "These handcrafted svg designs were created exclusively for the platform."
            }
        },
    }
</script>

<style scoped>

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