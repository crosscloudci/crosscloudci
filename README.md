# Cross-cloud Continuous Integration

### Why Cross-cloud CI?

The CNCF ecosystem is large, diverse and continues to grow. CNCF would like to ensure cross-project interoperability and cross-cloud deployments of all cloud native technologies and show the daily status of builds and deployments on a status dashboard. 

### What is Cross-cloud CI?


The Cross-cloud CI project consists of a cross-cloud testing system, status repository server and a dashboard. The cross-cloud testing system has 3 components (build, cross-cloud, cross-project) that continually validate the interoperability of each CNCF project for any commit on stable and head across all supported cloud providers. The cross-cloud testing system can reuse existing artifacts from a project’s preferred CI system or generate new build artifacts. The status repository server collects the test results and the dashboard displays them.

The Cross-cloud CI project is composed of 3 main components:

1. Cross-cloud testing system:
- Build Pipeline Stage per project (optional, can use project’s build artifacts)
  * Compiles binaries
  * Creates containers
- Cloud Provisioning Pipeline Stage, aka [Cross-cloud](https://github.com/crosscloudci/cross-cloud) 
  * Deploys K8s onto each cloud
- App Deployment Pipeline Stage, aka [Cross-project](https://github.com/crosscloudci/cross-project) 
  * Deploys containerized apps onto Kubernetes 
  * Runs upstream e2e tests for each project 
  * Supplies results to the Cross-cloud dashboard

2. Status Repository Server
   * Stores the interoperability status of CNCF projects

3. [Cross-cloud CI Dashboard](https://cncf.ci)
   * Displays a high-level view of the interoperability status of CNCF projects for each supported cloud provider.
  

### How to use the Cross-Cloud CI Project

* [Cross-Cloud Provisioner](https://github.com/crosscloudci/cross-cloud#how-to-use-cross-cloud)
* [Cross-Project App Deployer/Tester](https://github.com/crosscloudci/cross-project) 


### Meetings / Demos

#### Upcoming
- April 24th, 2018 - CI-WG Status Update
- May 2nd-4th, 2018 - [KubeCon CloudNativeCon Europe in Copenhagen, Denmark](https://www.google.com/url?q=https%3A%2F%2Fevents.linuxfoundation.org%2Fevents%2Fkubecon-cloudnativecon-europe-2018%2F&sa=D&ust=1515523215433000&usg=AFQjCNHskvq8WRzkzRNuh9A8rGjCJcvoyg)
- May 3rd, 2018 - [Intro to CNCF CI/WG and Cross-cloud CI project](https://kccnceu18.sched.com/event/DrnT/cncf-cicd-wg-intro)
- May 4th, 2018 - [Deep Dive for CNCF CI/WG and Cross-cloud CI project](https://kccnceu18.sched.com/event/DroD/cncf-cicd-working-group-deep-dive)
- May 8th, 2018 - CI-WG Status Update


#### Past
- [April 12th, 2018 - Cross-cloud CI project intro with VMware](https://docs.google.com/presentation/d/1p9ho9RkHdeja11wq20S_ctPbgEa_pY3KaETzfW87_Os/edit#slide=id.g24450b0d21_0_222)
- [April 11th, 2018 - Cross-cloud CI project intro with Spinnaker](https://docs.google.com/presentation/d/1cse3qkQgDWzF42I77X0Uo-00KID0Q4w3tZRpEw4zx-M/edit)
- [April 10th, 2018 - Cross-cloud CI project demo with Cluster Lifecycle SIG](https://docs.google.com/presentation/d/1qpUXDgK3TzK2lJWVN7YJJWMb-Lr37g-RdT4tDYXoRn0/edit#slide=id.g24450b0d21_0_222)
- [April 10th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1Cjyv-FD8hLbHG876jUeVQsGWHSezZrqZ0xJ83eDfHxA/edit) 
- [April 9th, 2018 - Cross-cloud CI project demo with IBM Cloud-Technical Overview](https://docs.google.com/presentation/d/160uOVQ7BDld5o7BCpPurbuSjAFfsESLEdP79fCu7GlQ/edit#slide=id.g24450b0d21_0_222) 
- [April 5th, 2018 - Cross-cloud CI project demo with IBM Cloud-ONAP Overview](https://docs.google.com/presentation/d/1VXmB4KVncDXO4cq4cBg8IfGOrbVlZc5xW7wsdmOrL9A/edit#slide=id.g24450b0d21_0_222) & [Recording](https://drive.google.com/file/d/1ahx3CHEjx_eG2i7JUYVFHXL5wSPmzLhF/view)
- [April 3rd, 2018 - CNCF TOC](https://youtu.be/uEPRv2a3Scs?t=975)
- [March 26th, 2018 - Cross-cloud CI + ONAP in ONS2018 Opening Keynote](https://youtu.be/eY2cHHMzOZw?t=1110)
- [March 24th, 2018 - Cross-cloud CI Overview at CI/CD Community Workshop](https://docs.google.com/presentation/d/1241RB9tJALXSFXJKbd7z3NU1mw06j_p6RnMKNcm0gAs/edit#slide=id.g24450b0d21_0_222)
- [March 13th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1yIZ8p8_3rqrT81rCsQtA1Burbfz6IAEF8wCsgOGT5Jc/edit#slide=id.g24450b0d21_0_222)
- [February 27th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1Yd2rH5PlwmhRoVCeIgI-kWpalRZ_ipgbtn5n0V58uRI/edit#slide=id.g24450b0d21_0_222)
- [February 13th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1J51D4uRLgS6o_J7xkHbQmVPxVjmceuYTr_we1MeCOI4/edit?ts=5a832888#slide=id.g24450b0d21_0_222)
- [January 26th, 2018 - Cross-Cloud CI Dashboard v1.0.0 Release](https://docs.google.com/presentation/d/1hhhx0C3REd3l94QU-0DB6Try4jdHZ8ou2klzJOfCC9M/edit?usp=sharing)
- [January 23rd, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1j8wa5xGMFFiLBwxuu4xyhtMFUyGSnDb-EIJY2ghsf-A/)
- January 18th, 2018 - Cross Cloud project demo with Lucas Käldström
- January 17th, 2018 - Cross Cloud project demo with Camille Fournier
- [January 9th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1DXs0DNCnPcpM8Bou6K1A3E9G89CmW8cwZJincwgewuM/edit#slide=id.g242b36cf7c_0_151)
- December 26th, 2017 - CI-WG Status Update on 4th Tuesday at 8am Pacific: Meeting canceled due to the holidays
- [December 12th, 2017 - CI-WG Status Updates](https://docs.google.com/presentation/d/16a-oKZcl4CKwMtcvU6mWDOzIcb7oNTXW5wNppN8-M0s/edit?usp=sharing)
- [December 6th-8th, 2017 - KubeCon + CloudNativeCon North America 2017](https://www.cncf.io/event/cloudnativecon-north-america-2017/)
- [November 28th, 2017 - CI-WG Status Updates](https://docs.google.com/presentation/d/1JAXkf6kKgo6E7mhKPgZXbRWIsh-yE6TkgEXPBhttpH4/edit?usp=sharing)
- [November 16th, 2017 - CNCF CI Cross Cloud project demo to OPNfv](https://docs.google.com/presentation/d/1_gfoyOWMWnt5YS1KuYSbKh-hHPYdgtQ4-lI3dPtaLSY/edit#slide=id.g27c85eba33_0_182)
- November 9th, 2017 - CNCF CI Cross Cloud project demo at End User Committee Meeting
- [November 8th, 2017 - CNCF CI Cross Cloud project demo to TensorFlow](https://docs.google.com/presentation/d/1AoJxg3PC84tAdKXNJ9t5PUUkBYTZjP9CQe197qokGZs/edit#slide=id.g24450b0d21_0_222)
- [November 2nd, 2017 - CNCF CI Cross Cloud project demo to Jez Humble, Continuous Delivery](https://docs.google.com/presentation/d/1dhJgeBLYEzXoVvpxX7ls75o-GdsVwhpUY08O8UAiUUc/edit?usp=sharing)
- [November 1st, 2017 - CNCF CI Cross Cloud project demo to Nic Jackson, Terraform](https://docs.google.com/presentation/d/1Y1E1y5SHTW56CDT4hyAFZAtPftOeezqCZrhLGCjY94A/edit?usp=sharing)
- [October 24th, 2017 - CI-WG Status Updates](https://docs.google.com/a/vulk.coop/presentation/d/10x7ssMrYN5A_XBxN8NBQ2Zoy2akbT2NqO7mn6hJLnSk/edit?usp=sharing)
- October 18th, 2017 - CNCF CI Cross Cloud project demo to Oracle Cloud
- [October 11th, 2017 - CNCF CI Cross Cloud project demo to ONAP](https://docs.google.com/presentation/d/1EclOrNbeF7gqlIR3hfjKAAVvdl68NDcWEGQho1MpS-E/edit#slide=id.g24450b0d21_0_222)
- [October 10th, 2017 - CI-WG Status Updates](https://docs.google.com/presentation/d/1kahPZZyk1S1fbvy0-ocaDvSzoJlSE_2JlE-sQHhDu1g/edit#slide=id.g242b36cf7c_0_10)
- October 3rd, 2017 - CNCF: OpenStack project demo
- September 27th, 2017 - CNCF: AWS project demo 
- September 12th, 2017 - CNCF: Governing Board
- September 11th-14th 2017 [Open Source Summit North America](http://events.linuxfoundation.org/events/open-source-summit-north-america)
- August 30th, 2017 CNCF/K8s Storage SIG Testing Group
- [August 22nd, 2017 - CI-WG ii.coop Status Updates](https://docs.google.com/presentation/d/1MixvezbkqJP4VeA09kUd-Po18V3SLHS-nSlOnkzowms/edit#slide=id.g242b36cf7c_0_10), [meeting recording](https://www.youtube.com/watch?v=TXZ151MRTpc)
- [August 15th, 2017 - CNCF TOC](https://youtu.be/aX12ituxdOU?t=51m32s)
- [August 8th, 2017 - CI-WG ii.coop Status Updates](https://docs.google.com/presentation/d/1dgkeXN7qSJ8tSUTZ5ecB67D155Y0Mphrpqi9ZFZXWKo/edit#slide=id.g242b36cf7c_0_10)
- [July 11th, 2017 - Kubernetes SIG Testing](https://www.youtube.com/watch?v=DQGcv2a4qXQ&list=PL69nYSiGNLP0ofY51bEooJ4TKuQtUSizR&index=1)
- [June 27, 2017 - CI-WG cross-cloud and containerops demos](https://www.youtube.com/watch?v=Jc5EJVK7ZZk&feature=youtu.be&t=307)
