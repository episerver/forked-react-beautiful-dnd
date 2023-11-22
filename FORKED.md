### Why this repo was forked?

the official repo from atlassian is here

https://github.com/atlassian/react-beautiful-dnd

the patched repo is here

https://github.com/casieber/react-beautiful-dnd

### PR to fix the issues between drag events & shadow Root is here and not merged yet in the official repo

https://github.com/atlassian/react-beautiful-dnd/pull/2319

Instead of using this fixed version as suggested in the comment
https://github.com/atlassian/react-beautiful-dnd/pull/2319#issuecomment-1269656861

and as the Axiom Team did here, adding a built lib inside axiom and using it in this user branch
https://jira.sso.episerver.net/browse/AX-969

https://github.com/optimizely/axiom/blob/user/hoshikitsunoda/AX-969-DragAndDrop-update-the-package-to-support-shadow-root/projects/axiom/src/libs/react-beautiful-dnd/index.js
and released "@optimizely/axiom": "^61.1.0-test.2",

with this package we were able to drag and drop correctly inside a Shadow root
https://jira.sso.episerver.net/browse/CMS-28999
https://github.com/episerver/content-edit-mfe/pull/48/files
using the <DragAndDrop> component exported from axiom

we probably should prefer to have a separate npm package, also because we want to work with Typescript
As suggested in the (last) comment  here

https://github.com/atlassian/react-beautiful-dnd/pull/2319#issuecomment-1270765451

the first internal forked package is now published here in the episerver scope

https://github.com/episerver/forked-react-beautiful-dnd/pkgs/npm/forked-react-beautiful-dnd

## OPEN Questions

types ?
original package types are here:

@types/react-beautiful-dnd
this package refers to the atlassian official one,
do we need to fork also the types package in order to have it working properly in our forked and patche one