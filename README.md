# Status based profiles for peer verified actions

## How it works

1. Users would take a picture and post it to their profile/ news feed (social media style)
2. Other users would vote 👍 or 👎
3. When a certain number of votes have been reached, points are awarded based on votes
    - TODO need to flesh out the economics here
4. All of this feeds into a tiered weekly leaderboard, as well as an all-time leaderboard

## Desired outcomes

- Users have profiles similar to social media dedicated to their actions
- Their actions are peer verified
- Raise awareness about individual actions that help focus are
- Peer pressure incentives to take individual actions that help focus area

## Actions

Actions are at the core of this system.
However, this system does not inherently contain any actions in itself.
Instead an an instance of this system may be spun up,
configured for a set of particular actions.

By default, it looks for actions within the `actions` directory,
and this may be overridden by using the `ACTIONS_DIR` environment variable.

Each action should be defined using a separate JSON file.
An example:

```json
{
  "type": "action/1",
  "id": "b35791172db3805530cd17039092fb0e68605a07cf3333931cb8cd761578734e",
  "version": 1,
  "disabled": true,
  "title": "Do something",
  "description": "A long form description of the action.\nMarkdown **is** permitted.",
  "checklist": [
    "A description of the first criterion required for this action to deemed to be done",
    "A description of the second criterion...",
    "A description of the final criterion",
  ],
  "actionTakerPoints": 100,
  "actionVerifierPoints": 10,
  "actionSharePoints": 1,
}
```

## Ideas for future improvement

- This system is designed around using photographs as evidence of actions.
  - What are forms can such evidence take?
  - Can the evidence be automated in any way?
  - How can we reduced the total number of steps needed by each actor?
- Encouraging users to work in teams
  - Enable users to connect with each other through a "follow"/ "friend" type mechanism
  - Enable users to connect with each other through their geographical proximity
  - Notify users when other connected users have taken a particular action
    - Follow up with a prompt to do the same action
    - Could offer bonus points to both this user and the connected users if all of them do it together
    - Could also notify the users that have already performed the action so that they might ask
      the user that they are connected to that has yet to perform the action to do so
- Weighted voting
  - Different users may have different votes carried on their votes
  - These weights could be calculated based on their level of involvement,
    as evidenced by their points, badges, and leaderboard positions,
    so as to give more involved users a higher say in the outcomes of claims
- Designing the relative weights of the points awarded for different actions
  - When new actions are added, users need to be incentivised to try them out.
  - When actions have different points, users are incentivised differently to try one action over another
  - Decide on a consistent formula for working out the baseline points for each action
  - Actions performed are temporal in nature
    - Could encourage repeats of a recently done action after a certain time period,
      by adjusting the points for that particular user
    - Could encourage repeats of an action done very long ago,
      by adjusting the points for that particular user
    - Could encourage a surge in particular regions by employing a "themed week",
      where bonus points are available for a particular subset of actions
      for the current week
  - Dynamic adjustment of points based on popularity
    - When a particular action is not done often enough,
      the points for performing that action could increase
    - When a particular action is done too often,
      the points for performing that action could decrease
- For actions that are grouped around a common theme,
  possibly create partnerships with organisations relevant to that theme.
  - If there are organisations that are willing to sponsor actions
    in this theme:
    - The sponsoring organisations could pay this system
    - The system could disburse these funds into other organisations
      which do the work for this theme
    - The users of this system, perhaps based on their level of involvement,
      could vote on which organisations would receive this work.
    - Organisations themselves could participate in the system by voting
      on the claims submitted by users
- Allow users to create new actions
  - The users of this system, perhaps based on their level of involvement,
    could vote on new actions to be added to the system
  - If the votes are sufficient to pass the new action,
    it gets added to the system with an incubation period
  - During the incubation period, if:
    - said action is taken by enough users,
      that is added permanently to the list of actions available in the system
    - said action is not taken by enough users,
      that action is removed, and is no longer possible to take
  - The votes to create new actions, their incubation, acceptance, and availability,
    could be restricted/ filtered
    - By geographical region
    - By level of involvement

## UML Sequence diagram

![Sequence diagram for status based profiles for peer verified actions](status-profiles-based-on-peer-verified-actions.plantuml.png)

## Licence

GPL-3.0

## Author

[Brendan Graetz](http://bguiz.com)
