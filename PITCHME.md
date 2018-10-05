---

# Pipelining Quality

[BaselOne](https://baselone.ch) - 16.10.2018

---
@title[about]
 
![me](https://github.com/MarkusTiede/about/raw/master/img/me-circle.png)

[@MarkusTiede](https://twitter.com/markustiede)

Software, Security & **Release Engineer** @ [Baloise](https://www.baloise.com)

+++

## @color[goldenrod](2 lessons learned)

@color[darkgreen](XX. best practices) & [YY. tools](https://en.wikipedia.org/wiki/Tool)

+++?image=https://github.com/baloise/talk-cicd-javascript/raw/master/img/baloise-park.jpg&size=contain

## @color[white](about/[baloise](https://www.baloise.com))

+++?image=http://amazingspace.org/resources/explorations/groundup/lesson/scopes/galileo/graphics/tele_galileo_big.jpg&size=contain

## about/[galileo](https://www.guidewire.com/about-us/news-and-events/press-releases/20160912/basler-versicherung-extends-guidewire-products)

+++?image=https://ak8.picdn.net/shutterstock/videos/15411808/thumb/2.jpg&size=contain

large-scale enterprise project

1.3k parallel sessions / day

4+ products

in- and outbound services

8 Scrum teams work in parallel

+++?image=https://upload.wikimedia.org/wikipedia/commons/4/43/Angry_elephant_ears.jpg&size=contain

## @color[white](some #numbers)
@color[white](Cluster of 4 * [2 + 1] nodes)

@color[white](~150 GB RAM / cluster)

@color[white](24/7 up-time)

@color[white](~30 min / rollout)

@color[white](30+ production releases per year)

---

## release management 

high-level goal: __knowledge__

1. dates: code-freeze, going-live
2. content: fixes, features, epics
3. quality: results, coverages

+++?color=lightgreen

## (un)known knowns: @color[goldenrod](predictability)

![](https://www.pmi.org/kasimage/10437c8a-9337-444f-8fa2-8f5318e93e71/p_1.jpg)

**fix** forecast of goals: dates / content / quality

+++?color=darkred

## (un)known unknowns: @color[goldenrod](flexibility)

![](https://www.pmi.org/kasimage/10437c8a-9337-444f-8fa2-8f5318e93e71/p_1.jpg)

on knowledge gain: **variable** re-definition of goals

e.g. other dates / other content / quality++

unknown → known

---?color=lightblue

## @color[darkgreen](1. traceability)

everything @color[darkgreen](digital and connected)

[Confluence ↔ JIRA](https://de.atlassian.com)
 
under @color[darkgreen](version control)

[git](https://git-scm.com)

---?color=lightblue

## @color[darkgreen](2. reproducibility)

@color[darkgreen](**automation** is key)

@color[darkgreen](**everything** as code)

application(s), service(s), build(s), test(s), environment(s), runtime(s)

+++?color=lightblue

## application(s) & service(s)

[Java 8](https://www.java.com/de/download/) and [Jakarta EE](https://jakarta.ee)

[Angular](https://angular.io)

+++?color=lightblue

## build(s)

[gradle](https://gradle.org) and [maven](https://maven.apache.org)

running in [Jenkins OSS](https://jenkins.io) pipelines

+++?color=lightblue

## test(s)

[Selenium](https://www.seleniumhq.org) and [TAF](https://github.com/baloise/test-automation-framework)

![](https://martinfowler.com/bliki/images/testPyramid/test-pyramid.png)

[JUnit](https://junit.org) and [Camunda BPMN Workflow Engine](https://camunda.com)

+++?color=lightblue

## environment(s), runtime(s)

[VM](https://en.wikipedia.org/wiki/Virtual_machine)s with [RHEL](https://en.wikipedia.org/wiki/Red_Hat_Enterprise_Linux) and [Liima](http://www.liima.org)

using [Ansible](https://www.ansible.com)

future: [OpenShift](https://en.wikipedia.org/wiki/OpenShift)

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

### @color[darkgreen](3. artifact repositories)
mostly for (semi) temporary time frames: max. 4 weeks

@color[darkgreen](continuous SNAPSHOTs)

1 x nightly @color[darkgreen](long-living SNAPSHOTs) / application

all @color[darkgreen](release candidates == **RELEASE**)

[Nexus Repository OSS](https://www.sonatype.com/nexus-repository-oss) 2 / 3

---

## @color[darkgreen](4. de-coupling)

---

## @color[darkgreen](5. parallelization)

branches
stacks
builds
deploys

---

## @color[darkgreen](6. sequentialize)

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
