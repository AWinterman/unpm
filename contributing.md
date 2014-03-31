Contributing
============

## Checklist:
- New code is covered by new tests and documentation. 
- Tests pass
- [jsl](https://www.npmjs.org/package/jsl) returns `checked n; OK` when run on
  every changed file.
- `package.json` contains all new dependencies you introduced.
- Your PR includes a description of your changes.

## So you want to contribute...

In the [issue tracker](https://github.com/hayes/unpm/issues?state=open),
enhancement requests and known bugs are listed according to the order in which
they were reported. If you want to work on one of these, please leave a comment
so that others do not duplicate your effort.

If you are uncertain how to proceed, feel free to comment on the issue with a
development plan you intend to follow. The maintainers will review it and
provide guidance as requested or required. 

If there is a new feature you would like to see, open a new issue, describe the
feature in English, and provide a sample of API usage if your proposal would
change it. Before you start, ask yourself if the feature could live as a stand
alone library or script, e.g. the [clone-packages][clone]  If it can, create
new repository for the project. When you are ready, publish it to a public
registry, preferably [npmjs.org](npmjs.org). Then submit a PR which updates
&mu;npm's package.json to include the new dependency, and update the
appropriate modules to add the feature.

[clone]: https://www.npmjs.org/package/clone-packages.

## You've written code to address the issue...

All contributions should made via [pull
request](https://help.github.com/articles/using-pull-requests) and review.
After a pull request is made other contributors will offer feedback. They will
approve your changes by leaving a +1 or an emoji as a comment on the PR. Once
you have two +1s from two different maintainers, the maintainers will merge
your changes.

If you've never made a PR before, you'll need to create a GitHub account, and
read GitHub's instructions on
[forking](https://help.github.com/articles/fork-a-repo) and [pull
requests](https://help.github.com/articles/using-pull-requests). Reading up on
the [git source control management system](http://git-scm.com/book) is also a
good idea.

Pull requests should be targeted at &mu;npm's `master` branch. Before pushing
to your GitHub repo and issuing the pull request, please run the full test
suite with the `npm test` command. It is your responsibility to fix any test
failures *before* asking for review. If you introduce code without tests, be
prepared to justify why it does not or cannot be tested. 

If you have modified the API, make sure to update the documentation
accordingly. Make a note of the API changes in the PR description as well, to
call out that the maintainers will have to update at least the minor version
number. (&mu;npm is [semantically versioned](http://semver.org/).)

We expect your code to pass our style guide, handily encoded by the package,
[jsl](https://www.npmjs.org/package/jsl). This is enforced by a
[test](./test/style.test.js') which runs the linter on all code which is every
run by a relative require from [./index.js](./index.js).

It is still up to you to verify any style on scripts, tests, or commands you
add. Before submitting your PR, `npm install -g jsl`, and then run `jsl` on all
such files you have changed. If it exits with a non-zero status code, expect
the maintainers to correct your style.

We will also review the substance of your code. Our philosophy is roughly:

- [Keep it simple](http://www.infoq.com/presentations/Simple-Made-Easy).
- [Avoid more abstraction than necessary](https://www.youtube.com/watch?v=_ahvzDzKdB0).
- Keep it documented.
- Keep it tested.
- Don't repeat yourself.
- Keep it small.

## Conduct

We operate under the Speak Up! project's [code of
conduct](http://speakup.io/coc.html).

## Communication

There is an IRC channel on irc.freenode.net called #unpm. You're welcome to
drop in and ask questions, discuss bugs and possible feature development, or
just hang out <3
