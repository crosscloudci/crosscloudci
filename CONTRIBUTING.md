Contributing to cncf.ci - CNCF CI Status Dashboard
---
Welcome! We gladly accept contributions from CNCF Project Maintainers and encourage you to get involved!

---
About cncf.ci
---

V2 of the CNCF CI status dashboard -- cncf.ci -- will provide a third party validation of builds, deployments and end-to-end testing for CNCF’s Graduated and Incubating projects. The CNCF CI status dashboard continually validates each CNCF project, for any commit on stable and head, running on Kubernetes clusters which are provisioned to a bare metal environment. The results of each testing stage are published to the cncf.ci status dashboard.

Upcoming iterations of the CNCF CI status dashboard will focus on supporting a sustainable and scalable project ecosystem. To accelerate adding & maintaining projects on cncf.ci, the status dashboard will integrate with a project’s existing CI System and accept contributions from CNCF project maintainers. 

**This page will be updated incrementally as each new opportunity for collaboration becomes available.**

---

Updating existing CNCF projects on cncf.ci: 
---

### Updating project details:

**What are the "Project Details" on cncf.ci?** 
-  Project's Logo
-  Project's Display Name 
-  Project's Subtitle
-  Project's GitHub Repo URL

![Project Details Example](https://user-images.githubusercontent.com/11701267/54546272-4f2d1f00-4971-11e9-9fb6-9cb42a8a997c.png)

**How can a CNCF Project Maintainer update Project Details?** 
Using Prometheus as an example:

1. Go to https://github.com/crosscloudci
1. Open the `project-configuation` repo for the CNCF Project, ie. [prometheus-configuration](https://github.com/crosscloudci/prometheus-configuration)
1. Open the `cncfci.yml` file, ie. [cncfci.yml](https://github.com/crosscloudci/prometheus-configuration/blob/master/cncfci.yml)
1. Click the "edit" icon
1. Create a new branch to make updates
1. Update content, as needed: 
   1. logo_url: (ie. "https://raw.githubusercontent.com/cncf/artwork/1d4e7cf3b60af40e008b2e2413f7a2d1ff784b52/prometheus/icon/color/prometheus-icon-color.png")
   1. display_name: (ie. Prometheus)
   1. sub_title: (ie. Monitoring)
   1. project_url: (ie. "https://github.com/prometheus/prometheus")
1. Submit a pull request to `master` branch
1. Tag reviewers as CNCF.CI project maintainers: @denverwilliams, @lixuna, @taylor, @wwatson
1. CNCF.CI project maintainer will review and merge pull request to `master` branch
1. CNCF.CI project maintainer will promote updated content 
1. Updated content will display on cncf.ci CNCF CI Status Dashboard

