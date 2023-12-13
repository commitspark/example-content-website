# Commitspark content example: Multi-language component-based Website

Follow these three steps to start using [Commitspark](https://commitspark.com) with this example content repository:

1. [Copy this template](https://github.com/commitspark/example-content-website/generate)
2. [Sign in to Commitspark using your GitHub account](https://commitspark.com/en-us/sign-in/)
3. Select your repository copy and start editing

All content you create will be written to plain text YAML files in your repository on GitHub.

## Content

In this example, we have a content model ready to manage content for a multi-language website built from different
content components.

It is meant as a starting-point for building your own content model by
[extending the schema file](commitspark/schema/schema.graphql) using standard GraphQL types.

## Workflows

An example GitHub workflow is included which demonstrates how content in pull requests can be validated using a QA
pipeline similar to those used in software development.

To trigger a failure in this example workflow, do the following:

1. Create a new branch
2. Create or modify a Page so that it contains a Hero component where the string `invalid` is included in the
Hero image's `imageId` field
3. Create a pull request to merge your branch into `main`
4. The workflow should now create a pull request comment that invalid content was found

Using [GitHub branch protection rules](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-protected-branches/managing-a-branch-protection-rule),
you can configure GitHub to disallow merging of a pull request when a workflow has failed. This means you can prevent
content that does not satisfy your QA criteria from being merged.
