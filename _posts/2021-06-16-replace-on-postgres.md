---
layout: post
title:  "How to replace the content of a field on postgre"
author: Indrajeet Gour
categories: [ postgres, tutorial ]
image: assets/images/3.jpg
toc: true
---
In many case we wanted to do just update/replace the some portion of the data from the column on one of the table on postgres DB.

So consider that we wanted to replace all the `indrajeet` to `prabodha` coming on field `name` on table `xyz` but I do not wanted to change the rest of the field.

## How I can do that
We juse have to use the REPLACE like mentioned below
```
UPDATE xyz SET name = REPLACE(name, 'indrajeet','prabodha');

```
It's depend on you how you wanted to use this with your usecase.
