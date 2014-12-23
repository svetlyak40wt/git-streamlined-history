git-streamlined-history
=======================

A test project for <allmychanges.com>.

Aim of this little repository is to
test if there is a command which outputs
git's history in a way applicable to
changelog generation. All commit
messages should appear in an order
in which they are merged into the current branch.

Here is the right command and order:

```
[art@allmychanges.com/test-repo]% git log --simplify-merges --no-merges
commit 556257f662ba963fc1bff5064555f2aa19f74f80
Author: Alexander Artemenko <svetlyak.40wt@gmail.com>
Date:   Tue Dec 23 05:58:44 2014 +0000

    Version 0.4.0

commit 52aebd85902794b6aecb9a389265cbba2a995295
Author: Alexander Artemenko <svetlyak.40wt@gmail.com>
Date:   Tue Dec 23 05:56:36 2014 +0000

    README added.

commit ebe7ceac2022b27a22903e46cb12b873f76d6ade
Author: Alexander Artemenko <svetlyak.40wt@gmail.com>
Date:   Tue Dec 23 05:57:45 2014 +0000

    Version 0.3.0

commit 695c749cca592709fa762eba2971f70318b16ef6
Author: Alexander Artemenko <svetlyak.40wt@gmail.com>
Date:   Tue Dec 23 05:55:43 2014 +0000

    Version 0.2.0

commit 3365a02292d7687dff591b26041fc8a6ded0de0b
Author: Alexander Artemenko <svetlyak.40wt@gmail.com>
Date:   Tue Dec 23 05:55:09 2014 +0000

    Initial
```

Look at the `README added.` commit. It was created before
`Version 0.3.0`, but merged after. And it appears in
right order. "Right" here is an order in which a code was
introduced in a given branch.
