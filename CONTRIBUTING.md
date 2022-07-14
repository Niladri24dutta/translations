# Contributing Guidelines

:+1::tada: Love you long time for wanting to help make FetLife better! :tada::+1:

These are just guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.


## How FetLife Manages Translations

To manage our translations we use GitHub. If you've ever programmed you are probably familiar with GitHub, or at the very least, version control.

If you are not familiar with GitHub, then it can be overwhelming at first, but once you get comfortable with it you will wonder how you ever lived without it.

The best place to learn about GitHub is through the [GitHub Guides](https://guides.github.com).


## Helping Out

You can help out in multiple ways, and you don't even need to be multilingual to do so:

- [Report any grammatical issues](https://github.com/fetlife/translations/issues) you come across in any language, including English, on FetLife.
- Submit improvements to our existing translations by clicking on the pencil in the right hand corner of every file.
- Translate FetLife into a language you are well versed in creating a new file with the proper language code, copying the contents of en.yml into the new file, translating as many strings as you can, and finally submitting the translation in a pull request to us.


Note: It's not always easy to review new additions to our translations so please help out and:

- Document what you changed in detail
- Make small PRs

Here's a great example of how it's done: https://github.com/fetlife/translations/pull/303


## Coding Conventions

Please try to always write a clear log message for each of your commits. One-line messages are fine for small changes, but bigger changes should be a bit meatier.


## Helpful Commands

To add missing keys to all translation files:

```
bundle exec i18n-tasks add-missing
```

To order the keys:

```
bundle exec i18n-tasks normalize
```

To remove a key from all translation files:

```
bundle exec i18n-tasks data -f yaml | bundle exec i18n-tasks tree-filter forgot_password.email.error_quota | bundle exec i18n-tasks data-remove
```
