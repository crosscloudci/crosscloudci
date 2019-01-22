![Cross-cloud Continuous Integration](https://raw.githubusercontent.com/crosscloudci/artwork/914eca80b90ad1325c9e2460a0410f4aaaaf3f69/crosscloudci/horizontal/color/crosscloudci-horizontal-color.png)



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

- [February 26th, 2019 - CI-WG Status Update](https://docs.google.com/presentation/d/1DQRpAbHU96jfSX6JFYFi_eZewQ-AP8kjoeGcucu5FxI/edit#slide=id.g3e44af8930_0_0)

#### Past
- [January 22nd, 2019 - CI-WG Status Update](https://docs.google.com/presentation/d/1NbRstXKJU7y7rOV60gV4Hg2TY2sM6l3rche73XpiRRk/edit#slide=id.g3e44af8930_0_0)
- [December 11th, 2018 - Intro: CNCF Cross-cloud CI at KubeCon+CloudNativeCon Seattle](https://kccna18.sched.com/event/Grci)
- [December 12th, 2018 - Deep Dive: CNCF Cross-cloud CI at KubeCon+CloudNativeCon Seattle](https://kccna18.sched.com/event/Greb) 
- [November 27th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/172GdH46mKj8pSx7yVTOg3d4BkwOJ3Wlt6_Pu09qYayI/edit#slide=id.g3e44af8930_0_0)
- [November 14th, 2018 - Intro: CNCF Cross-cloud CI at KubeCon+CloudNativeCon China](https://kccncchina2018english.sched.com/event/FuL2)
- [October 23rd, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1OkFQvmPnfMZjNZtpe0irfax01llm2ziWUq-V9i2HUN8/edit#slide=id.g3e44af8930_0_0)
- [September 25th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1wB922KAXg3Z8a-TNizoTm8WoDIVF7i9uIYtitmvwSSY/edit#slide=id.g3e44af8930_0_0)
- [August 28th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1n2vwXjKgaohCfEIp4li2SQqWPvYhvHSRLZJKEiqGvKk/edit?usp=sharing)
- [July 24th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1i6_s3gnAv5nuPMbtKDs4wNuQfjY1ZCNHl9eWPXEdfjw/edit#slide=id.g3c7ed1ecb6_0_0)
- [June 26th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1ugLK-QUv0yfb8qiCS41MW8__I58TrHYu4rzhck4CbpM/edit#slide=id.g3c7ed1ecb6_0_0)
- [May 22nd, 2018 - CI-WG Status Update & Recap of Cross-cloud CI V1 Goals](https://docs.google.com/presentation/d/19CTi4_k0Cjf6KKFd21TBSxTBDeyiiDalcw08ELxeaqI/edit#slide=id.g3783789093_0_269)
- [May 4th, 2018 - Deep Dive for CNCF Cross-cloud CI project](https://docs.google.com/presentation/d/1fpUdXYV230ciZPb-EHveKCkQUW2Fz63lsHjG4Lt1qlg/edit#slide=id.p3) & [Recording](https://youtu.be/m-WK-pOs5TA)
- [May 3rd, 2018 - Intro to CNCF Cross-cloud CI project](https://docs.google.com/presentation/d/1mpcuGlP5yzvKmYYOFB0L9WWSFPUnhIQ1E2jT8ko6bqc/edit#slide=id.p3) & [Recording](https://youtu.be/wb7aCAk1VFU)
- [April 24th, 2018 - CI-WG Status Update](https://docs.google.com/presentation/d/1jGp_qyMA877k5hnThiJkS1Rr1e-tVb8L2CcDGmSbscU/edit#slide=id.g3783789093_0_269)
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


### In the news:
- [CNCF + LFN collaborate on VNFs to CNFs](https://www.enterprisetimes.co.uk/2018/10/01/cncf-lfn-collaborate-on-vnfs-to-cnfs/)
- [The Linux Foundation to Drive Shift to Container Network Functions](https://containerjournal.com/2018/10/05/the-linux-foundation-to-drive-shift-to-container-network-functions/)
- [Linux Foundation Networking & Cloud Native Computing Foundation Get Jiggy](https://www.lightreading.com/nfv/containers/linux-foundation-networking-and-cloud-native-computing-foundation-get-jiggy/d/d-id/746403)
- [The Linux Foundation Brings Network Automation and Cloud Native Communities Together as Network Functions evolve to CNFs](https://www.prnewswire.com/news-releases/the-linux-foundation-brings-network-automation-and-cloud-native-communities-together-as-network-functions-evolve-to-cnfs-300718287.html)
- [Linux Foundation helps blend automation and cloud-native communities](https://www.fiercetelecom.com/telecom/linux-foundation-helps-blend-automation-and-cloud-native-communities)
- [Google sets Kubernetes free with $9m in its pocket for expenses](https://www.theregister.co.uk/2018/08/30/google_kubernetes_project/)
- [CNCF Adds VMware vSphere to Cross-Cloud CI Dashboard](https://blogs.vmware.com/cloudnative/2018/07/24/cncf-adds-vmware-vsphere-to-cross-cloud-ci-dashboard/)
- [OpenStack Foundation Publishes White Paper on Containers Integration, Highlights Cross-Community Accomplishments](https://goo.gl/mkCdiL)
- [Kubernetes 1.10 and Cross-Cloud CI Project Dashboard 1.3 Released, and Kubernetes Survey Announced](https://www.infoq.com/news/2018/04/kubernetes-1.10-cross-cloud)
- [CNCF: Containerize Your Legacy!](https://www.lightreading.com/nfv/containers/cncf-containerize-your-legacy!/d/d-id/741954)
- [CNCF Launches Cross-Cloud CI Project & Adds ONAP Networking Project to Dashboard Overview](https://www.cncf.io/blog/2018/03/27/cncf-launches-cross-cloud-ci-project-adds-onap-networking-project-to-dashboard-overview/)
- [ONAP, CNCF Come Together on Containers](https://www.lightreading.com/nfv/containers/onap-cncf-come-together-on-containers/d/d-id/741790)
- [CNCF Unveils Continuous Integration Platform for Kubernetes](https://containerjournal.com/2018/03/27/cncf-unveils-continuous-integration-platform-kubernetes/)
- [Kubernetes Ecosystem Grows as Cloud Native Computing Foundation Expands](https://www.serverwatch.com/server-news/kubernetes-ecosystem-grows-as-cloud-native-computing-foundation-expands.html)
- [CNCF, Packet Provide Free Infrastructure for Cloud Developers](https://thenewstack.io/cncf-packet-team-provide-free-infrastructure-cloud-developers/)
