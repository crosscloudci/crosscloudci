# FREQUENTLY ASKED QUESTIONS


## What does the Cross-cloud CI workflow look like:

- At 3 AM Eastern Time, a scheduled job runs:
  - Build latest releases - using build artifacts or downloading project’s existing artifacts
  - Provision clouds with K8s - deploy K8s to resources
  - Deploy the apps and run e-2-e test
  - Deprovision, destroy VMs

## How can we make sure the new cloud is not showing FAILED on cncf.ci?

- Failed badges are most commonly caused by resources not available for the Cross-cloud testing system when the scheduled job runs at 3am Eastern Time
- Ensure that the new cloud has available resources for Cross-cloud CI
