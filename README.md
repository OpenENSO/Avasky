# Avasky - BETA

---


Avasky is a gateway to other services. One can think of it as a hub or, as we like to call it, a decentralized workstation. You can use it to setup your project/business resources and grant access to all via one account, which is created using SkyID. To make sure the user is using one account and is verified as a truly unique human, we have setup BrightID integration, which links services to one identity. BrightID is a privacy-friendly service which can verify the identity and human status of a user without betraying confidentiality. Furthermore, we shall explain each service being used, as well as their functionality and how to replicate those actions.

Link to application: [Avasky](https://siasky.net/_AHq4sJ27VwL4f8g0yQL6Xh6-HkhVjN6o7KsGkDjwrwFCg/)

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

2. The 'PROFILE' page of Avasky is used to first authenticate a user with the help of a 3box profile. If the user doesn't have one, the service will create one automatically.
It also makes sure to sync the profile data and deliver them should that be the need. (Needs integration and testing)

3. To verify their uniqueness and connected service, the user hovers over the logo and will be presented with a link. Once clicked, it will generate a QR code to scan which opens the BrightID app. Then their verification status is queried, returning either a 'Verified' or 'Not verified' title on their profile page, as well as the application which has been linked to their account.

Details: the link, once clicked, calls the 'uuid4' function for generating a contextID. This, in turn, gets sent to the 'deep link' and gets encoded as a QR to scan.

## TODO

1. Enable full profile sync, setup storage and communication using SkyID and Skynet.
2. Enlist Avasky add-ons to BrightID node operators and integrate sponsorships.
3. Enable email filters for the 'LOGIN' capability.
4. Enforce better verification for BrightID.

## Further details and vision

Avasky is an extensible, straightforward, customizable gateway for anyone seeking to give their project or business an easy manner of authentication and providing human uniqueness. 

We aim to make Avasky as adaptable as possible, capable of being tailored to the needs of any project, all while keeping a clutterless UI and fluid UX, focused both on user and business. Of course, we do not forget our principles: keeping it decentralized ( 3box & Skynet), clean ( Magic Links ) and human-friendly ( BrightID ).

This project was created with love and care by Motanovici, an year III student of CS. Submission project for the : Build with BrightID and SkyDB Debut hackathons!
