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

+++?color=lightgreen

## reproducibility
### == pipelining

lessons learned

best practices & tools

---

## automate
everything* as code

version controlled

*application(s), service(s), test(s), environment(s), runtime(s), pipeline(s), work- and data-flows

---

### snapshots

+++

### theory

<canvas data-chart="line">
<!-- 
{
 "data": {
  "labels": ["Mo"," Tu"," We"," Th"," Fr", "Mo"," Tu"," We"," Th"," Fr"],
  "datasets": [
   {
    "data":[0,15,25,35,45,55,65,75,85,100],
    "label":"team 1","borderColor":"rgba(20,220,220,1)"
   },
   {
    "data":[0,10,20,30,40,50,60,70,80,100],
    "label":"team 2","borderColor":"rgba(220,120,120,1)"
   },
   {
    "data":[0,5,15,25,35,45,55,65,75,100],
    "label":"team 3","borderColor":"rgba(135,206,250,1)"
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
  "labels": ["Mo"," Tu"," We"," Th"," Fr", "Mo"," Tu"," We"," Th"," Fr"],
  "datasets": [
   {
    "data":[0,15,25,25,20,40,55,50,65,60],
    "label":"team 1","borderColor":"rgba(20,220,220,1)"
   },
   {
    "data":[0,35,20,30,45,55,60,75,70,75],
    "label":"team 2","borderColor":"rgba(220,120,120,1)"
   },
   {
    "data":[0,5,15,20,30,35,45,55,60,70],
    "label":"team 3","borderColor":"rgba(135,206,250,1)"
   }
  ]
 }, 
 "options": { "responsive": "true" }
}
-->
</canvas>

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

## reproduce

---

## golden data / master

---

## knowledge (graphs)

---

## monitor
