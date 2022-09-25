
### Building Cremini Using Ceramic - A Short Story

The goal of our team has always been to help the community grow and prosper. We tried in many directions.

When we first decided to build [Cremini](https://ethglobal.com/showcase/cremini-x9wth), we were inspired by Gitcoin Passport. The user experience is fantastic. Why dont we build a community reputation system, starting from discord guilds, just on this cool versioned version of IPFS :)?

The team started off very well. By following the tutorial we soon finished code of the key-did stream read/write, and learned Ceramic's technical principles. I have to admit that the learning curve started to get steeper for us backend programmers from here.

We wanted to improve user experience: 1 After user authorizes for the first time, we can automatically update the onchain profile as a trusted third party. 2 Users can use, for example, the address of the Ethereum wallet as did.

We found that 3id can be used for key rotation, and it can be fully controlled by the user's blockchain wallet. Awesome, these two functions were exactly what we want!

But after careful researching, we did not find simple examples of implementing key rotation. The 3ID-connect package which can support in browser blockchain wallets was also unfriendly to our backend programmers. We spent a lot of time here.

On a video call with Matthew (cool guy, awesome!), he showed us the projects Ceramic team was working on: DID-Session and ComposeDB. The former does not need to rely on the frontend, has pkh-did support, has user-controlled authorization, and has easy-to-use serialization and deserialization functions. The latter has the indexing support and data aggregation we want to use in our plan.

A while after the call, our team completed the code snippet of did session. I have to say that this library is really convenient, but it is hidden in a deep position on Ceramic's official website, and the did-js-org website is not easy to find in the search engine.

We have studied the example of ComposeDB. But due to time constraints, we will integrate it on ETHBogota, to index and query reputation data and explore the possibility of integrating with other data models (for example, gitcoin passport is an ideal integration object). At that time we will launch the Reputation SDK. We'll be spending more time getting familiar with it recently.