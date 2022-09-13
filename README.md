# 측정 가능한 어플리케이션 만들기
Measurable Application with Springboot Actuator, Prometheus, Grafana

## 개요
어플리케이션은 분석, 설계, 개발, 테스트, 운영이라는 라이프사이클을 갖는다.

이 모든 단계에서 어플리케이션이 정확히 구현되었는지, 주어진 상황에서 요청된 기능을 원할하게 처리하고 있는지를 알 수 있는 방법은, 시스템의 CPU, Memory, Disk 등의 자원 모니터링을 통해 확인하는 것이 일반적이다.

다만, 이 방법은 간접적인 측정이어서 어플리케이션의 기능 단위의 관찰이 어려운 단점이 있다.

또한, MSA가 대두되면서 어플리케이션은 배치는 다이나믹한 구성과 복잡한 호출관계를 가지게 되었다.

이러한 문제를 해결하는 근본적인 방법은 어플리케이션이 각각의 상황을 지수화하여 외부에 노출 할 수 있도록 하는 것이다. 

지수화한 어플리케이션 내부의 데이터를 우리는 메트릭(Matrics)라고 부르며, 이를 구현해보고 OSS 모니터링 솔루션을 활용화여 시각화 하여본다.

## 학습 목표
* OSS 모니터링 시스템인 Prometheus, Grafana를 배포, 구축할 수 있다.
* 예제 어플리케이션(PetClinic)을 배포하고, Grafana를 통해 Matrics을 조회할 수 있다.
* 커스텀 메트릭을 추가할 수 있다.

## 목차

1. 어플리케이션 모니터링: 개요
  1.1 프로파일링, 트레이싱, 로깅, 메트릭
  1.2 Prometheus, Grafana
  1.3 Spring boot actuator

2. 인프라 구성
  2.1 wsl2
    - wsl2 설치, ubuntu 22.04 설치, vscode 설치
  2.2 podman, Prometheus, Grafana
    - podman, podman-compose 설치, Prometheus 설치, Grafana 설치
  2.3. Springboot Actuator Sample: petclinic
    - petclinic 

3. Springboot 
