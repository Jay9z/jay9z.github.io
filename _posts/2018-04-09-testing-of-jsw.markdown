---
layout: post
title: "testing of jsw"
date: "2018-04-09 13:18:52 +0800"
---
## "tb" connections

match (n:pin)-[rel]->(n1:pin)
where n.pinType="tb" or n1.pinType='tb'
return n.fullName,rel.sequence,rel.chapter_details,n1.fullName
order by rel.sequence


## all connections

match (n:pin)-[rel]->(n1:pin)
return n.fullName,rel.sequence,rel.chapter_details,n1.fullName
order by rel.sequence

## all connections of insulation type

match (n:pin)-[rel:insulation]->(n1:pin)
return n.fullName,rel.sequence,rel.chapter,n1.fullName
order by rel.sequence

## all connections of continuity type

match (n:pin)-[rel:continuity]->(n1:pin)
return n.fullName,rel.sequence,rel.chapter,n1.fullName
order by rel.sequence
