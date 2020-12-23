# Avasky - BETA

---


Avasky is a decentralized workstation focused on humans. That means we use BrightID to verify your stamp of uniqueness on the network and grant certain priviliges based on that trust, like: staying social and getting access to various resources.

BrightID is a privacy-friendly social identity network which can verify the uniqueness and Jarvis status of a user without betraying the confidentiality of their data.

Furthermore, we shall explain each service being used, as well as their functionality and how to replicate those actions.

Link to application: [Avasky](https://siasky.net/_AVA17NJFRI-7o9814OUjBmHXojiHICYScYcra-30DCANQ)

Video DEMO ( For BrightID - remaking ) : [Demo video]()

## BrightID



BrightID allows us to add a decentralized verification capability to Avasky, all while maintaining privacy. It does so by creating 'deep links' between your account and the application currently registered on BrightID node operators. You get verified by other users by participating in meetings and as such, a far more reliable and human connection is being established. This is a far better solution to the usual and very annoying 'captcha'. Not only this, but it is a handy way to integrate multiple services and keep track of all under the banner of one account. We are also using BrightID to redirect you to a service once you are verified as a human on the network ( still under development - heavily dependent on issue #687 - see below )

## What are Skylinks?



We are using a decentralized storage platform called Skynet ( powered by Sia ) for storage and extended decentralized functionalities. As an example, we created a skapp called Skydrop, an add-on for the Avasky service which enables quick content sharing via skylinks.

The SDK empowered us to easily connect our application to Skynet and make use of a reliable and responsive platform.

## How to use Avasky

1. If you wish to add your own services to Avasky, then clone this repo and open the file 'login.html'.
Then, proceed to change the 'href' value of the following code:

```
window.location.href = "https://siasky.net/_AE85qV8kEbLqYbXF0ZOhRKU2Q_4XD_MwPSrTdEQM_-PNw/";

```
Once you are verified you will gain access to these resources.

2. The 'PROFILE' page of Avasky is used to allow the user to view their social stamp on the network and see basic information about their accounts. We have also offered the following features: A BrightID verification system ( explained below ) - the user hovers over the logo and a QR code is there for scanning. Once finished, the user can click on the 'Get linked' functionality in order to update their profile.

**TIP** : Your BrightID can be found by accessing the following portal: [BrightID Explore](https://explorer.brightid.org/). You can then go ahead and login using BrightID credentials, after which you will be shown your BrightID and place in the huge social graph of the network.

3. To verify their uniqueness and connected services, the user can scan a QR code which will redirect them to the BrightID mobile app for approval. This is done by first assigning a contextID ( using uuidv4 ) and generating a deep link with it. This link is, in turn, encoded as a QR code using the QRious JS library.

4. The 'RESOURCES' page of Avasky can be used to get access to custom resources using BrightID. I chose BrightID because of the potential I believe it has and because it fits to the vision I have for Avasky. It can be an identity verification solution, as well as a means to socializing and granting access to various resources by virtue of the aforementioned system.


## TODO

1. Solve BrightID Issue #687 - allows, for example, the BrightID connection between 2 users of the Avasky workstation and much more.
2. Add decentralized storage to Avasky for profiles and other data ( looking into SkyDB )
3. Remaking the application in React and integrating BrightID functionalities using SDK.
4. Proper login using BrightID once point no. 1 is solved
5. Establish a proper algorithm for the 'Ava trust score' depending on the connections, status and BrightID score.

## Further details and vision

Avasky is an extensible, straightforward, customizable workstation for anyone seeking to give their project or business an easy manner of authentication and providing human uniqueness.

We aim to make Avasky as adaptable as possible, capable of being tailored to the needs of any project, all while keeping a clutterless UI and fluid UX, focused both on user and business. Of course, we do not forget our principles: keeping it decentralized ( Skynet ), human-friendly and seamless ( BrightID ).

This project was created with love and care by Motanovici. Submission project for the : 'Build with BrightID' hackathon!
