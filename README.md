# Commitspark example: Content Management for a Multi-language Component-based Website

In this example repository for [Commitspark](https://commitspark.com), we provide a data model to manage content for
a multi-language website that is built from individual content building blocks.

The example is meant as a starting-point for building your own data model by
[extending the schema file](commitspark/schema/schema.graphql) using standard GraphQL types.

## Setup

Follow these steps to start working with this example:

1. [Copy this template](https://github.com/commitspark/example-content-website/generate)
2. Ensure the [GitHub App](https://github.com/commitspark/frontend?tab=readme-ov-file#github) you use to authenticate
   users in the Commitspark [data editing frontend](https://github.com/commitspark/frontend) with GitHub grants access
   to this new repository
3. Sign in to your Commitspark frontend instance
4. Select your repository copy and start editing

## GitHub Workflow Example

An example GitHub workflow is included in this repository which demonstrates how content in pull requests can be
validated using a QA pipeline equivalent to those used in software development.

To trigger a failure in this example workflow, do the following:

1. On GitHub, create a new branch
2. In the Commitspark editing frontend, select the new branch and create or modify a Page so that it contains a Hero
   component where the string `invalid` is included in the Hero image's `imageId` field
3. On GitHub, create a pull request to merge your new branch into `main`
4. The workflow should now create a pull request comment that invalid content was found

Using [GitHub branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule),
you can configure GitHub to disallow merging of a pull request when a workflow has failed. This means you can prevent
content that does not satisfy your QA criteria from being merged.
