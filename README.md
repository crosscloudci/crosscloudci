# Cross-cloud Continuous Integration

### Why Cross-cloud CI?

The CNCF CI Working Group has been tasked with building a cross project and cross cloud test system that compliments existing project CI systems which tests the interoperability of projects within the CNCF ecosystem across multiple cloud providers. The results of the tests should be publicly accessible from a user friendly dashboard.

### What is Cross-cloud CI?


A project to continually validate the interoperability of each CNCF project, for every commit on stable and HEAD, for all supported cloud providers with the results published to the Cross-cloud public dashboard. The Cross-cloud project is composed of the following components:
- [Cross-cloud](https://github.com/crosscloudci/cross-cloud) Cross-cloud - Multi-cloud kubernetes provisioner
  * Creates K8s clusters on cloud providers
  * Supplies conformance validated Kubernetes end-points for each cloud provider with cloud specific features enabled
- [Cross-project](https://github.com/crosscloudci/cross-project) - Project app and e2e test container builder / Project to Cross-cloud CI integration point
  * Deploys containerized apps and runs upstream project tests supplying results to the Cross-cloud dashboard.
  * Builds and registers containerized apps as well as their related e2e tests for deployment.
- [Cross-cloud CI Dashboard](http://cncf.ci)
  * Provides a high-level view of the interoperability status of CNCF projects for each supported cloud provider.

The [CNCF CI Dashboard](http://cncf.ci) shows the latest results of testing for CNCF projects/clouds (supported and active).

### How to use the Cross-Cloud CI Project

* [Cross-Cloud Provisioner](https://github.com/crosscloudci/cross-cloud#how-to-use-cross-cloud)
* [Cross-Project App Deployer/Tester](https://github.com/crosscloudci/cross-project) 


### Meetings / Demos

#### Upcoming
- March, 2018 - Intro call with Packet+Arm team, TBD
- March 24th-25th, 2018 - [Cross Community Infra and CICD F2F/Workshop in Los Angeles](https://public.etherpad-mozilla.org/p/cross-community-infra-cicd)
- March 26th-29th, 2018 - [ONS North America 2018 in Los Angeles](https://events.linuxfoundation.org/events/open-networking-summit-north-america-2018/)
- May 2nd-4th, 2018 - [KubeCon CloudNativeCon Europe in Copenhagen, Denmark](https://www.google.com/url?q=https%3A%2F%2Fevents.linuxfoundation.org%2Fevents%2Fkubecon-cloudnativecon-europe-2018%2F&sa=D&ust=1515523215433000&usg=AFQjCNHskvq8WRzkzRNuh9A8rGjCJcvoyg)



#### Past
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
