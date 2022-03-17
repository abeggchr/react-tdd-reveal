# Invitation

# Preparation

- Start presentation (both)
- Have Editor ready (enable prettier/autosave/jest extension)
- Start application
- Have empty CRA ready: `npx create-react-app tdd-b --template typescript`
- Before we start: it's important to always know whether you are in the green or in the red. To visualize I wrote a reporter using my Phillips Hue lamps. Add this to package.json:
- ` "test.hue": "react-scripts test --reporters='default' --reporters='../../hue-reporter/hue-reporter.js'",`

# Talk

## Introduction to TDD (Nick)

Slides:

- Chapter 1: TDD (Christian)
- Chapter 2: Testing React (Nick)

Changes / comments to the slides:

### What is TDD?

Mention storybook

## Hands On

### Goal

Show application "react-tdd-code"

### What's the first, simplest test case?

### Start coding

Steps:

- What's the first, simplest test case? > Title // Discussion: granularity of tests (testing title?)
- Implement:
- Show title
- Shows empty cart
- Products list in app -> ugly: products array in App
- Refactor: refactor component to take props
- Skip: Refactor: data > as props (refactor to Shop component)
- Adds item to cart functionality
- Refactor to Shop

Extension:
- Tomato is multiple times on the Shop after adding it to the cart -> how to test?
  - appears twice -> ok
  - appears in cart:   const cart = screen.getByTestId("cart"); getByTestId(cart, "Test");

Challenges with TDD:

- how fine grained?
  - test title or not?
  - how big of a step are you taking?
- when to extract components?
  - saw it with ProductList, Shop
- how to load (test) data?
  - as props
  - in store
  - fake backend
- structuring
  - show describe (what) / describe (state, render) / test

## Discussion

## But wait, what about Redux

Redux examples:

- connected [cha](https://trassee-4.zuehlke.com/tfs/Project_c13774/FA%20Trassee/_git/FA%20Trassee%20Sources?version=GBmaster&path=%2FSources%2FTra%2FMistra.Tra.Web.React%2Fsrc%2Fpages%2Fnormen%2Fcomponents%2FNormenPage.test.tsx)
-> 111, redux state
-> 52, mocked backedn
- container component [nipa]

## Impact on your work

- I have spent more time writing tests than implementing the feature.
- A big part was understanding it, especially in the beginning. Typically the framework is optimized for fast development. Testing comes on top and you have to understand what's going on

i.e.

- when to await, when not (animations)
- library (how does it render)

## Impact to test suite

- more tests
- more like system tests (also due to testing-library)

## Impact on team

- you are the slow one (applies always when you are the one caring for clean code, tests, ...)
-

## Is there a situation where not to use TDD

- POC (make it a throw away POC!)
- non-productive stuff, elaboration etc.

## What about the promises

Yes

- Be confident that your code works
- Less debugging

Well...

- Fast feedback / continous reward
  - test suite grows fast, takes a lot of time to execute
  - having a test suite of the stuff you are woking on now is cumbersome
- Frequent and safe refactorings
- still needs discipline

## Feedback from project

How does it feel?