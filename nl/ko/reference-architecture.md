---
copyright:
  years: 2016,2018
lastupdated: "2018-06-13"
---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}

# 아키텍처 
{: #architecture}

## 복제

{{site.data.keyword.composeForRedis_full}} 서비스에서는 [Redis Sentinel](https://redis.io/topics/sentinel)을 사용하여 데이터베이스의 고가용성 및 모니터링을 제공합니다. 각 서비스는 세 개의 데이터 노드로 구성되며, 세 개 모두 sentinel 프로세스를 실행하고 두 개는 redis 프로세스를 실행합니다. 서비스가 배치되는 영역을 선택하면 세 개의 노드가 영역의 가용성 구역에 분산되고 데이터가 해당 구역 전체에 복제됩니다. 한 데이터 멤버에 연결할 수 없게 되어도 클러스터는 계속 정상적으로 작동합니다.

## 디스크 암호화

모든 {{site.data.keyword.composeForRedis}} 서비스의 암호화는 사용되지 않습니다. 데이터는 볼륨 레벨 암호화가 사용된 서버에 있습니다. 

{{site.data.keyword.composeForRedis}}은 관리 서비스이므로 {{site.data.keyword.cloud}} Compose 운영자가 데이터를 볼 수 있습니다. 디스크 암호화 외에도, 데이터베이스에 개인 정보를 저장하는 경우 저장하기 전이나 데이터베이스 자체에서 암호화를 사용하는 기능 또는 확장기능을 사용하여 정보를 암호화하는 것이 좋습니다. 해당 메소드는 사용성이나 성능에 영향을 미칠 수 있지만 암호화를 통해 개인 정보를 보호하는 것이 좋습니다.

## Auto-Scaling

리소스는 Redis 데이터베이스의 총 메모리 사용을 기반으로 자동으로 스케일링됩니다. 스토리지는 1:1로 프로비저닝된 RAM의 비율을 기반으로 합니다. 해당 리소스는 단위로 번들됩니다.

Auto-Scaling은 데이터베이스의 중단기 상태동향에 대응하도록 설계되었습니다. 매분 서비스를 확인하고 RAM이 부족하면 더 많은 단위가 배치에 할당됩니다. 

Auto-Scaling에서는 디스크/메모리 사용량이 줄어든 배치의 스케일은 줄이지 않습니다. 데이터베이스에 프로비저닝된 리소스는 나중에 필요한 경우를 대비하여 그대로 남아 있거나 배치의 스케일을 수동으로 축소할 때까지 그대로 남아 있습니다.
{: .tip}
