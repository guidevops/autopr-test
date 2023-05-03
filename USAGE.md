# Getting Started with AutoPR

This guide will walk you through setting up and using AutoPR, the GitHub Action that automatically writes pull requests in response to issues.

## Prerequisites

Before getting started, ensure you have:

- A GitHub repository for your project. Alternatively, you can use the [AutoPR-template](https://github.com/irgolic/AutoPR-template/) to create a new repository.
- An OpenAI API key with access to ChatGPT.

## Setup

Follow these steps to set up AutoPR in your GitHub repository:

1. Create a new file in your repository named .github/workflows/autopr.yml and add the contents from [the AutoPR-template workflow YAML file](https://github.com/guidevops/autopr-test/blob/main/.github/workflows/autopr.yml).
Follow these steps to set up AutoPR in your GitHub repository:

1. Create a new file in your repository named .github/workflows/autopr.yml and add the contents from [the AutoPR-template workflow YAML file](https://github.com/guidevops/autopr-test/blob/main/.github/workflows/autopr.yml).
2. In your GitHub repository settings, navigate to Secrets and variables -> Actions and add your OpenAI API key as OPENAI_API_KEY.
3. In your GitHub repository settings, go to Actions -> General and scroll down to Workflow permissions. Enable Allow GitHub Actions to create and approve pull requests.
4. Create a label in your repository that contains the string "AutoPR" (e.g., "Run AutoPR rocket" or simply "AutoPR").
3. In your GitHub repository settings, navigate to Secrets and variables -> Actions and add your OpenAI API key as OPENAI_API_KEY.
4. In your GitHub repository settings, go to Actions -> General and scroll down to Workflow permissions. Enable Allow GitHub Actions to create and approve pull requests.
5. Create a label in your repository that contains the string "AutoPR" (e.g., "Run AutoPR rocket" or simply "AutoPR").

## Usage

To use AutoPR, follow these steps:

1. Create a new issue in your GitHub repository with a clear and concise description of the task or bug fix.
2. Add the AutoPR label to the issue. This will trigger the AutoPR workflow.
3. Once the action is triggered, it will create a new branch named autopr/issue-# and open a pull request to the base branch. If the branch already exists, it will be overwritten.
4. Review the generated pull request and make any necessary adjustments.
5. Merge the pull request into the base branch once you're satisfied with the changes.
