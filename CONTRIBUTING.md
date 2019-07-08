Contributing to cncf.ci - CNCF CI Status Dashboard
---
Welcome! We gladly accept contributions from CNCF Project Maintainers and encourage you to get involved!

**This page will be updated incrementally as each new opportunity for collaboration becomes available.**

---
About cncf.ci
---

V2 of the CNCF CI status dashboard -- cncf.ci -- will provide a third party validation of builds, deployments and end-to-end testing for CNCF’s Graduated and Incubating projects. The CNCF CI status dashboard continually validates each CNCF project, for any commit on stable and head, running on Kubernetes clusters which are provisioned to a bare metal environment. The results of each testing stage are published to the cncf.ci status dashboard.

Upcoming iterations of the CNCF CI status dashboard will focus on supporting a sustainable and scalable project ecosystem. To accelerate adding & maintaining projects on cncf.ci, the status dashboard will integrate with a project’s existing CI System and accept contributions from CNCF project maintainers. 

---

Updating existing CNCF projects on cncf.ci: 
---

### Updating project details:

**What are the "Project Details" on cncf.ci?** 
-  Project's logo in svg format
-  Project's display name 
-  Project's subtitle
-  Project's GitHub repo URL

![Project Details Example](https://user-images.githubusercontent.com/11701267/54546272-4f2d1f00-4971-11e9-9fb6-9cb42a8a997c.png)

**How can a CNCF Project Maintainer update Project Details?** 
- Using Prometheus as an example:

1. Go to https://github.com/crosscloudci
1. Open the `project-configuation` repo for the CNCF Project, ie. [prometheus-configuration](https://github.com/crosscloudci/prometheus-configuration)
1. Open the `cncfci.yml` file on the `master` branch, ie. [cncfci.yml](https://github.com/crosscloudci/prometheus-configuration/blob/master/cncfci.yml)
1. Click the "edit" icon
1. Create a new branch to make updates
1. Update content, as needed: 
   1. logo_url: "https://raw.githubusercontent.com/cncf/artwork/master/prometheus/icon/color/prometheus-icon-color.svg?sanitize=true" (for svg format, append ?sanitize=true to url)
   1. display_name: (ie. Prometheus)
   1. sub_title: (ie. Monitoring)
   1. project_url: (ie. "https://github.com/prometheus/prometheus")
1. Submit a pull request to `master` branch
1. Tag reviewers as CNCF.CI project maintainers: @denverwilliams, @lixuna, @taylor, @wwatson
1. CNCF.CI project maintainer will review and merge pull request to `master` branch
1. Updated content will display on cncf.ci CNCF CI Status Dashboard

### Updating release details:

**What are the "Release Details" on cncf.ci?** 
-  Project's latest stable release
-  Project's latest commit on master branch

![Release Details Example](https://user-images.githubusercontent.com/11701267/60830121-2036f500-a17c-11e9-8e7e-5db2a443f3b3.png)

**How can a CNCF Project Maintainer update Release Details?** 
- Using CoreDNS as an example:

1. Go to https://github.com/crosscloudci
1. Open the `project-configuation` repo for the CNCF Project, ie. [coredns-configuration](https://github.com/crosscloudci/coredns-configuration)
1. Open the `cncfci.yml` file on the `master` branch, ie. [cncfci.yml](https://github.com/crosscloudci/coredns-configuration/blob/master/cncfci.yml)
1. Click the "edit" icon
1. Create a new branch to make updates
1. Update content, as needed: 
   1.   stable_ref: "v1.5.2"
   1.   head_ref: "master"
1. Submit a pull request to `master` branch
1. Tag reviewers as CNCF.CI project maintainers: @denverwilliams, @lixuna, @taylor, @wwatson
1. CNCF.CI project maintainer will review and merge pull request to `master` branch
1. Updated content will display on cncf.ci CNCF CI Status Dashboard
