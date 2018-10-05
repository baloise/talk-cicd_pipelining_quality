---

# Pipelining Quality

[BaselOne](https://baselone.ch) - 16.10.2018

---
@title[about]
 
![me](https://github.com/MarkusTiede/about/raw/master/img/me-circle.png)

[@MarkusTiede](https://twitter.com/markustiede)

Software, Security & Release Engineer @ [Baloise](https://www.baloise.com)

+++?image=https://github.com/baloise/talk-cicd-javascript/raw/master/img/baloise-park.jpg&size=contain

## @color[white](about/[baloise](https://www.baloise.com))

+++?image=http://amazingspace.org/resources/explorations/groundup/lesson/scopes/galileo/graphics/tele_galileo_big.jpg&size=contain

## about/[galileo](https://www.guidewire.com/about-us/news-and-events/press-releases/20160912/basler-versicherung-extends-guidewire-products)

+++?image=https://ak8.picdn.net/shutterstock/videos/15411808/thumb/2.jpg&size=contain

large-scale insurance enterprise project

1.3k parallel internal sessions / day

4 products: PolicyCenter, BillingCenter, ContactManager and end-user portal solution(s)

many in- and outbound services

8 Scrum teams work in parallel in 2 week sprints

+++?image=https://upload.wikimedia.org/wikipedia/commons/4/43/Angry_elephant_ears.jpg&size=contain

## @color[white](some #numbers)
@color[white](JBoss cluster of 4 * [2 + 1] nodes)

@color[white](~150 GB RAM / cluster)

@color[white](24/7 up-time)

@color[white](~30 min / rollout)

@color[white](30+ production releases per year)

---?color=lightgreen

## quality

+++?color=lightcoral

## knowlegde

+++?color=lightblue

## reproducibility
### == pipelining

lessons learned

best practices & tools

---?color=lightblue

## keep track

all digital and connected

[Confluence ↔ JIRA](https://de.atlassian.com)
 
under version control

[git](https://git-scm.com)

---?color=lightblue

## automate
**everything** as code

application(s), service(s), build(s), test(s), environment(s), runtime(s), pipeline(s), work- and data-flows

+++?color=lightblue

## application(s) & service(s)

[Java 8](https://www.java.com/de/download/) and [Jakarta EE](https://jakarta.ee)

+++?color=lightblue

## build(s)

[gradle](https://gradle.org) and [maven](https://maven.apache.org)

+++?color=lightblue

## test(s)

[Selenium](https://www.seleniumhq.org) and [TAF](https://github.com/baloise/test-automation-framework)

![](https://martinfowler.com/bliki/images/testPyramid/test-pyramid.png)

[JUnit](https://junit.org) and [Camunda BPMN Workflow Engine](https://camunda.com)

+++?color=lightblue

## environment(s), runtime(s)

VMs, [RHEL](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux), [Liima](http://www.liima.org)

[Ansible](https://www.ansible.com)

[OpenShift](https://en.wikipedia.org/wiki/OpenShift)

---?image=https://i.imgur.com/RVvnuO5.jpg&size=contain
@title[snapshots]

+++

### sprint theory

<canvas data-chart="line">
<!-- 
{
 "data": {
  "labels": ["We","Th","Fr","Mo","Tu","We","Th","Fr","Mo","Tu"],
  "datasets": [
   {
    "data":[0,15,25,35,45,55,65,75,85,100],
    "label":"Team 1","borderColor":"rgba(20,220,220,1)"
   },
   {
    "data":[0,10,20,30,40,50,60,70,80,100],
    "label":"Team 2","borderColor":"rgba(220,120,120,1)"
   },
   {
    "data":[0,5,15,25,35,45,55,65,75,100],
    "label":"Team 3","borderColor":"rgba(135,206,250,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>

+++

### real world

<canvas data-chart="line">
<!-- 
{
 "data": {
  "labels": ["We","Th","Fr","Mo","Tu","We","Th","Fr","Mo","Tu"],
  "datasets": [
   {
    "data":[0,15,25,25,20,40,55,50,65,60],
    "label":"Team 1","borderColor":"rgba(20,220,220,1)"
   },
   {
    "data":[0,35,20,30,45,55,60,75,70,75],
    "label":"Team 2","borderColor":"rgba(220,120,120,1)"
   },
   {
    "data":[0,5,15,20,30,35,45,55,60,70],
    "label":"Team 3","borderColor":"rgba(135,206,250,1)"
   },
   {
    "data":[0,25,10,35,20,45,30,55,40,65],
    "label":"3rd party dependencies","borderColor":"rgba(144,238,144,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>

+++?color=lightblue

### (dust-)bin(ary) repositories
mostly for (semi) temporary time frames: max. 4 weeks

continuous SNAPSHOTs

1 x nightly long(er)-living SNAPSHOT / application

all RCs (release candidates) == **RELEASE**

[Nexus Repository OSS](https://www.sonatype.com/nexus-repository-oss) 2 / 3

---

## de-couple

---

## parallelize

branches
stacks
builds
deploys

---

## sequentialize

T -> I -> A -> P

batches

---

## no exceptions

MAJOR == MINOR == MICRO == HOTFIX

---

## golden data / master

---

## knowledge (graphs)

---

## monitor
