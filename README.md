# Highload Software Architecture 8 Lesson 24 Homework

Continuous Deployment
---

## Project setup

This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

Just a default Next.js project, can b run with `npm run dev`.

The CI/CD pipeline is configured in the `.github/workflows` directory. It uses GitHub Actions to build and deploy the project to the AWS EC2 instance as a Docker container.

The pipeline consists of two workflows: [`docker-image.yml`](.github/workflows/docker-image.yml) and [`aws-deploy.yml`](.github/workflows/aws-deploy.yml).

The first workflow builds the Docker image and pushes it to the AWS ECR repository.

The second workflow pulls the image from the ECR repository and deploys it to the AWS EC2 instance.

The results of the pipeline can be seen in the [Actions tab](https://github.com/serhii-samoilenko/hsa-homework-24/actions) of this repository.
