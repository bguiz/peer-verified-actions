## Development roadmap

Minimum viable product (MVP):

- Begin with the development of the leaderboard
  - New NodeJs project init
  - Design the database schema
  - Implement the weekly leaderboard
  - Implement the cron job
  - Implement the promotions/ demotions mechanism
- Move on to the server
  - New NodeJs project init
  - Implement handle new claim
  - Implement handle add claim verification part 1,
    where new votes are recorded
- Move on to the immutable data store
  - New Truffle project init
  - Write smart contract function to handle verified claims
- Move back to the server
  - Implement handle claim verification part 2,
    where to handle vote threshold met scenario
- Move onto the client
  - New vanilla JS/ HTML/ CSS project init
  - Implement a utility function for signing data
    following the EIP-712 standard
  - Create page with a form for claim submission
  - Create page with a form for claim verification submission
  - Create sub-page template that displays a claim,
    verified or unverified
  - Create sub-page template that displays a badge
  - Create page that fetches and displays a user profile
  - Create page that fetches and displays the feed

All other features are post-MVP.
The order in which they are implemented is expected to be
heavily influenced by the learnings/ discoveries
during the development of the MVP.
Thus the roadmap for that is intentionally left out.
