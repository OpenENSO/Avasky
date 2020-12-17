# Avasky - BETA

---


Avasky is a gateway to other services. One can think of it as a hub or, as we like to call it, a decentralized workstation. You can use it to setup your project/business resources and grant access to all via one account, which is created using SkyID. To make sure the user is using one account and is verified as a truly unique human, we have setup BrightID integration, which links services to one identity. BrightID is a privacy-friendly service which can verify the identity and human status of a user without betraying confidentiality. Furthermore, we shall explain each service being used, as well as their functionality and how to replicate those actions.

Link to application: [Avasky](https://siasky.net/_AGDogb10q-BxiNoOxhR1SXJWGfNLojWNVGRtylInModiQ/)

## BrightID



BrightID allows us to add a decentralized verification capability to Avasky, all while maintaining privacy. It does so by creating 'deep links' between your account and the application currently registered on BrightID node operators. You get verified by other users by participating in meetings, thus adding a human experience to the app. This is a far better ( far more reliable ) solution to the usual and very annoying 'captcha'. Not only this, but it is a handy way to integrate multiple services and keep track of all under the banner of one account. 

## What are Skylinks?



We are using a decentralized storage platform called Skynet ( powered by Sia ) for storage and extended decentralized functionalities. As an example, we created a skapp called Skydrop, an add-on for the Avasky service which enables quick content sharing via skylinks.

The SDK empowered us to easily connect our application to Skynet and make use of a reliable and responsive platform.

## SkyID

We chose SkyID for authenticating the user and run the service under the banner of one account. It is fully compatible with other applications built on Skynet and allows further extensions such as comments and storage. It also helps us keep true to our ethos of a decentralized service as it enables us with dID and ensures interoperability with other applications.

## Magic Links



Magic Links offer an SDK for 'passwordless logins'. The service allows you to authenticate via email by verifying a certain link, as well as implement social and WebAuthn logins.

We use this service to grant access to specific resources given an email. The application is fully customizable and the UI as well UX
are kept at the same level of friendliness and fluidity.

## How to use Avasky

1. If you wish to add your own services to Avasky, then clone this repo and open the file 'login.html'.
Then, proceed to change the 'redirectURI' value of the following code:

```
const handleLogin = async (e) => {
        e.preventDefault();
        const email = new FormData(e.target).get("email");
        if (email) {
          /* One-liner login */
          await magic.auth.loginWithMagicLink({ 
			email,
			redirectURI: 'https://siasky.net/_AE85qV8kEbLqYbXF0ZOhRKU2Q_4XD_MwPSrTdEQM_-PNw/'
		  });
          render();
        }
      };

```
Once the 'redirectURI' has been changed, the user will automatically get redirected to your custom service.

2. The 'PROFILE' page of Avasky is used to authenticate a user with the help of SkyID and see basic information about their accounts. We have also offered the following features: A BrightID verification system ( explained below ) - the user hovers over the logo and a QR code is there for scanning. Once finished, the user can click on the 'Get verified' functionality in order to update their profile.

3. To verify their uniqueness and connected services, the user can scan a QR code which will redirect them to the BrightID mobile app for approval. This is done by first assigning a contextID ( using uuidv4 ) and generate a deep link with it. This link is, in turn, encoded as a QR code using the QRious JS library.

4. The 'RESOURCES' page of Avasky can be used to get access to custom domains via the use of Magic Links. Provide an email and accept the link - you will automatically get redirected to the default add-on for Avasky: Skydrop.


## TODO

1. Enable full profile sync, setup storage and communication using SkyID and Skynet.
2. Enlist Avasky add-ons to BrightID node operators and integrate sponsorships.
3. Enable email filters for the 'LOGIN' capability.
4. Enforce better verification for BrightID.
5. Save profiles to a skylink, allowing the user to share or update it. Setup BrightID profiles.

## Further details and vision

Avasky is an extensible, straightforward, customizable gateway for anyone seeking to give their project or business an easy manner of authentication and providing human uniqueness. 

We aim to make Avasky as adaptable as possible, capable of being tailored to the needs of any project, all while keeping a clutterless UI and fluid UX, focused both on user and business. Of course, we do not forget our principles: keeping it decentralized ( SkyID & Skynet), human-friendly ( BrightID ) and seamless ( Magic Links ).

This project was created with love and care by Motanovici, an year III student of CS. Submission project for the : Build with BrightID and SkyDB Debut hackathons!
