## System technologies

The system comprises of the following parts:

- Client
  - **Implemented with**: Web application
    - **Future implementations**: Android application,
      iOS application
  - **User features**:
    - User sign up
    - User log in/ log out
    - Take photo
    - Sign and submit claim
    - Sign and submit claim verification
    - Receive and display notifications from:
      Server, leaderboard, immutable data store
    - Fetch and display user profile
    - Fetch and display claim details
    - Fetch and display feed
    - Fetch and display weekly leaderboard
    - Fetch and display all-time tiered leaderboard
    - Fetch and display badges
    - Generate URL unfurl data for shares on social media
  - **Technical features**:
    - HTTP requests/ responses
    - Websocket connections
    - ECDSA for digital signatures
    - Form verification
- Server
  - **Implemented with**: NodeJs + ExpressJs
  - **User features**:
    - Handle take action request
    - Handle verify action request
    - Retrieve user profile
    - Retrieve claim
    - Retrieve feed
  - **Technical features**:
    - HTTP requests/ responses
    - Websocket connections
    - Stateless request handling
    - JWT based authentication and authorisation
    - Error logging
    - Keep track of usage statistics for reports
    - Relay communications between client and
      immutable data store
    - Relay communications between client and
      leaderboard
- Leaderboard
  - **Implemented with**: NodeJs + ExpressJs
  - **User features**:
    - React to new verification event
    - React to successful claim event
    - React to unsuccessful claim event
    - Manage promotions/ demotions of users between tiers
    - Manage assignment of users to new leaderboards
      every week
    - Retrieve weekly leaderboard
    - Retrieve all-time tiered leaderboard
    - Retrieve badges
  - **Technical features**:
    - HTTP requests/ responses
    - Websocket connections
    - Stateless request handling
    - JWT based authentication and authorisation
    - Error logging
    - Keep track of usage statistics for reports
    - Relay communications between client and
      immutable data store
    - Relay communications between client and
      leaderboard
- File store
  - **Implemented with**: CDN
    - **Future implementations**:
      IPFS, Swarm
  - **User features**:
    - Handle upload picture
    - Handle download picture
  - **Technical features**:
    - Provide hash or unique ID for uploaded images
    - Provide persistent storage of images
- Mutable data store
  - **Implemented with**: PostgreSql, Redis
  - **User features**:
    - (none)
  - **Technical features**:
    - Store relational data
    - Query relational data
    - Cache LRU data
- Immutable data store
  - **Implemented with**: EVM-based smart contract
  - **User features**:
    - (none)
  - **Technical features**:
    - Append-only writes of new data leveraging properties of a blockchain
    - Data stored in an key-addressable manner
      using smart contracts
    - Emit events
