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

## UML Sequence diagram

![Sequence diagram for status based profiles for peer verified actions](status-profiles-based-on-peer-verified-actions.plantuml.png)

## Licence

GPL-3.0

## Author

[Brendan Graetz](http://bguiz.com)
