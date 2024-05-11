# Review: Variables Lab

## Learning Goals

- Practice using `const` and `let` to declare variables in JavaScript

## Instructions

In this lab we'll practice declaring and assigning values to variables. We'll
also go over how to read the test document. Understanding how to read the tests
can be a valuable tool in figuring out exactly what you'll need to do to
complete the lab.

### Tests

When we want to run an experiment, we need to develop a hypothesis and we need
to test it. In programming, we run tests to verify that programs behave the way
we think they do. Tests help us identify bugs and judge how healthy our
applications are.

We use tests to describe the program's behavior, just as you would in a
professional coding environment, and we also use them as teaching tools. You are
in charge of getting the tests to pass.

### Structure

The structure of this lab — where its files and folders are located
— looks roughly like the following:

``` text
├── CONTRIBUTING.md
├── LICENSE.md
├── README.md
├── index.js
├── node_modules/
├── package.json
└── test
    └── indexTest.js
```

All labs will more or less have the same structure. (And non-lab lessons, for
that matter, will still have CONTRIBUTING.md, LICENSE.md, and README.md files.)

### Code Along

This lesson is set up as a code-along, so you'll first need to **fork and
clone** it to your local environment.

**Quick Review:**

**1.** Click the **Octocat** icon in the upper right of this page. This will
bring you to GitHub. Click the **Fork** button. Verify that your GitHub username
is showing in the **Owner** dropdown, then click the **Create
fork** button.

**2.** Once your fork is created, click the **Code** button in GitHub, make sure
**SSH** is selected, and copy the provided git URL info.

**3.** Make sure you're in `Development/code/phase-1` (or wherever you're
storing your code for the course) and clone the repo to your local machine with
`git clone` followed by the git URL you copied.

```console
$ git clone git@github.com:your-github-username/phase-1-javascript-variables-lab.git
```

**4.** The previous command will create a folder in the `phase-1` folder
containing your fork of this lab's repository. `cd` into the repository that you
just cloned down in the terminal, then run `code .` to open the files in Visual
Studio Code.

```console
$ cd phase-1-javascript-variables-lab
$ code .
```

Open up `index.js` in your code editor; you should see, well, nothing. We'll fix
that soon.

Now open up `test/indexTest.js`. Hey, there's something! What's all of this
stuff doing?

**Note:** The `test/indexTest.js` has great info that we want to look at, but do
not edit this file otherwise you may have extra difficulty passing this lab.

A few lines down in the `test/indexTest.js` file you will see:

```js
describe('index.js', function () {
  // there's stuff in here, too
});
```

`describe` is a function provided by our test library, Mocha, and it's used to
hold our tests. After the word `describe` is information about our tests. Tests
are used as a way to document the behavior of a function to developers. For
example, the next word `describe` is followed by the word `companyName`. Here
the test is telling us that the tests that come afterwards will be about
`companyName`. Then comes the word `it`, where you see the following:

```js
it('is set as Scuber', function () {
  // tests are here
});
```

This is telling us that the `companyName` should be set to `Scuber`. Finally,
filling in the missing part of the `it` code, we see:

```js
it('is set as Scuber', function () {
  expect(companyName).to.equal('Scuber');
});
```

This example shows that the test expects `companyName` to equal `Scuber`. That
`expect` and `to.equal` are essentially doing the same thing as `companyName ==
'Scuber'`. In other words, `expect(companyName).to.equal('Scuber')` is running
code that will have this first test pass if `companyName` equals `Scuber` and
fail if it does not.

Don't worry too much yet if it's hard to understand what is happening inside of
the `test/indexTest.js` file. But it's a good idea to open up the file, and
gather the information that you can. We will also provide instructions in the
`README.md` file that will allow you to complete the lab.

