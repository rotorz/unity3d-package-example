# unity3d-package-example

An example npm package that contains some example assets to demonstrate how to create a
package for use in games made using the Unity game engine.


## A peek inside package.json

The most important observation is the keyword `unity3d-package` because this is used by
the `unity3d-package-syncer` utility to detect npm packages that are designed to be used
with the Unity game engine.

The `unity3d` keyword is entirely optional although may be useful when searching for
Unity specific packages on the npm registry.


## The 'assets' directory

The name of this directory must be lower case. Any files contained within this directory
will be copied into the Unity project when the `unity3d-package-syncer` utility is
executed.

Each asset file inside the 'assets' directory should be accompanied with its corresponding
`.meta` file so that the Unity serializer can preserve links between assets.


## Extra files that are also synchronized

The `LICENSE` and `README.md` files are copied from the root directory of the package when
the `unity3d-package-syncer` utility is executed when they are present.

Likewise the `package.json` file will also be copied from the root directory of the
package when the `unity3d-package-syncer` utility is executed. This is necessary so that
the `unity3d-package-syncer` utility can compare the version of the package inside the
Unity project with the one that is currently installed in the project's `node_modules`
directory.


## What happens to any other files or directories?

Aside from the 'assets' directory and the other extra files that are mentioned above; no
further files or directories are copied from the npm package. This means that your npm
package can include things like unit testing, solutions, projects, makefiles, etc.


## Contribution Agreement

This project is licensed under the MIT license (see LICENSE). To be in the best
position to enforce these licenses the copyright status of this project needs to
be as simple as possible. To achieve this the following terms and conditions
must be met:

- All contributed content (including but not limited to source code, text,
  image, videos, bug reports, suggestions, ideas, etc.) must be the
  contributors own work.

- The contributor disclaims all copyright and accepts that their contributed
  content will be released to the public domain.

- The act of submitting a contribution indicates that the contributor agrees
  with this agreement. This includes (but is not limited to) pull requests, issues,
  tickets, e-mails, newsgroups, blogs, forums, etc.
