## Saltstack User State

This state relies heavily on a Gist by [UtahDave](https://gist.github.com/UtahDave/3785738).
It's just a little bit tweaked for the sake of more flexibility.

So one can define pillars for users to be present as for users to be absent (examples are included).

## Dependencies

There needs to be a *groups.sls* state and pillar as shown at the mentioned gist.
I may provide that in an extra repository as well.

## Examples

Remember that no group state or group pillar is included but can easily be adopted from the gist above.

states / top.sls

    base:
    '*':
      - users
      - groups

pillars / top.sls

    base:
    '*':
      - groups
      - users

