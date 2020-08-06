# Potential bug when building
For some reason Yarn wouldn't load all the necessary packages into node_modules when doing a simple `yarn [install]`.

I resolved this locally with the following command: `yarn workspaces focus sanity-studio`

One way to figure this is the error would be to look at the number of packages beginning with "slate" in node_modules.
If that number is lower than 10, which is the correct number at the time, you probably have the aforementioned bug.

Another symptom would be an error message like the one below when running `yarn build`:

>Error: Errors while building:
 /Users/mikael/git/yarn_unfocused_issue_repro/node_modules/slate-plain-serializer/lib/slate-plain-serializer.es.js
 Module not found: Error: Can't resolve 'slate' in '/Users/mikael/git/yarn_unfocused_issue_repro/node_modules/slate-plain-serializer/lib'


# Sanity Clean Content Studio

Congratulations, you have now installed the Sanity Content Studio, an open source real-time content editing environment connected to the Sanity backend.

Now you can do the following things:

- [Read “getting started” in the docs](https://www.sanity.io/docs/introduction/getting-started?utm_source=readme)
- [Join the community Slack](https://slack.sanity.io/?utm_source=readme)
- [Extend and build plugins](https://www.sanity.io/docs/content-studio/extending?utm_source=readme)
