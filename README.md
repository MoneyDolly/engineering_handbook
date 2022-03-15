# The MoneyDolly Engineering Handbook

As a member of the MoneyDolly Development team, you are an essential part of facilitating the success of student fundraisers
across the country. We have a high degree of trust with all of our team members, and firmly believe that you know your skills,
strengths, and experiences better than anyone else. This handbook is intended to be a guide on some best practices and philosophies
for you to consider in combination with your own experiences to ensure that you are doing the most valuable thing you could possibly
be doing each day.

## Guiding Philosophy

At MoneyDolly our north star is to make students' fundraisers as successful as possible, as efficiently and lean as possible.

This means that we need to consider both what is immediately most efficient (what is the minimum we can do to provide the most value),
as well as what is going to allow us to continue to be efficient into the future.

For example:

* When implementing a customer-facing feature, efficiently likely means: automated testing, automated pipelines, automated infrastructure, etc to
  ensure that we can maintain high code quality and maintainability well into the future.


* When implementing a one-off internal dashboard, efficiently likely means a trade-off of less maintainability _now_ in order for us to provide that
  value immediately.

With that being said, there are two areas that we **never** want to compromise on:

* Security: We are often dealing with sensitive student information that we **must** protect. This means that we are always following best practices, and never taking shortcuts.


* Data Integrity: Although our server going down for a few minutes is something that we want to avoid, it's likely something that our customers can forgive us for. Irrecoverably losing all of their order information is not. We need to ensure we are always taking backups, reviewing migrations, and planning for "how can this be undone".

## Project Management

We currently use a Kanban project management system to provide just enough structure around the development process to make sure that
we are not lost at sea, while still allowing us to be nimble, lean, and agile (with a little a). Our project management process should do
everything it can to support our guiding philosophy, and not be something that gets in the way or impedes work actually getting done.

* Note: We say "currently" as process should always be an ongoing discussion. What works best for us today may not work best for us tomorrow.

Kanban requires a high level of communication within the team we maintain our flow. If you have questions, get blocked, or discover a task is
likely to take the next 6 months instead of 2 days, it's expected that you will be proactive and reach out as needed. This is especially important
in a remote environment.

Although t-shirt size estimates may be asked from time to time for prioritization, we understand that engineering is inherently a creative
pursuit and not factory work. We trust that everyone is doing their best work, and just ask that everyone is kept updated on status and
expectations if something does not go as planned.

## Git Strategy

We currently use a [GitFlow](https://datasift.github.io/gitflow/IntroducingGitFlow.html) strategy to manage our code and deployment process.
Feature branches should be short-lived and rebased onto develop frequently to ensure that we always have a consistent version of the codebase.

GitLab CI/CD is set up to automatically compile and test every change pushed to our repo, as well as automatically deploy to our staging and
production environments.

## Code Reviews

All changes at MoneyDolly should go through a code review process -- whether that's a junior developer making their
first commit _ever_, or the tech lead. Similarly, everyone on the team, regardless of seniority, will be expected to participate in
code reviews as it's a great way to get multiple perspectives, and can often expose people to areas of the codebase they
may not yet be familiar with.

We strive to automate as much of the "boring" feedback as possible. Code formatting and linting should be handled by CI, instead of
having engineers debate about it in merge requests.

Since code reviews can often take a lot of time for the reviewer, the submitter should provide as much context as they can
for _why_ they went with a specific approach over another (after all, the submitter is the most familiar with the change, right?).

* Why was the change made? Bugfix? Refactoring? New feature?


* Did we use a specific pattern here?


* Anything specific to look out for when testing?


* If visual (such as in a front-end change, or a report), provide an example "output" screenshot or pdf showing that the change works as expected

## Communication

With MoneyDolly being a completely remote team, communication is as important as raw technical talent. Often this will take
an asynchronous form in slack, or comment in a ticket. Proactively reaching out when: you get stuck, are unsure of what to work on next,
or are passing a ticket onto someone else are musts to ensure that everyone is working as best they can.

When in doubt, error on the side of over-communication and dial it back as needed, rather than the other way around.



