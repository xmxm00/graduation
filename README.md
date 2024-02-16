# 백송현 졸업논문 연구노트

> LKD = Linux Kernel Development 3rd edition, ULK = Understanding the Linux Kernel 3rd edition

- 230914 LKD CH3 (Process Management) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-3.-Process-Management)
- 230919 LKD CH4 (Process Scheduling) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-4.-Process-Scheduling)
- 230926 LKD CH5 (System Calls) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-5.-System-Calls)
- 230930 졸업논문 서약서 및 제안서 작성 완료
  컨테이너 가상화 환경의 효율적인 자원 관리에 관한 분석
- 231004 LKD CH7 (Interrupts and Interrupt Handlers) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-7.-Interrupts-and-Interrupt-Handlers)
- 231009 LKD CH8 (Bottom Halves and Deferring Work) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-8.-Bottom-Halves-and-Deferring-Work)
- 231011 LKD CH9 (An Introduction to Kernel Synchronization) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-9.-An-Introduction-to-Kernel-Synchronization)
- 231019 LKD CH10 (Kernel Synchronization Methods) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-10.-Kernel-Synchronization-Methods)
- 231024 LKD CH12 (Memory Management) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-Ch12.-Memory-Management)
- 231107 LKD CH13 (Virtual Filesystem) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-Ch13.-Virtual-Filesystem)
- 231110 LKD CH14 (The Block I/O Layer) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-Ch14.-The-Block-IO-Layer)
- 231116 LKD CH16 (The Page Cache and Page Writeback) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-Ch16.-The-Page-Cache-and-Page-Writeback)
- 231122 LKD 1회독 완료 및 면담

  Github 연구노트 관리 및 연구주제 설정에 대한 면담. 논문 작성 일정 및 학회 일정 등 내용 공유. LKD를 반복하여 이해하며 ULK를 병행학습

- 231206 LKD CH15 (The Process Address Space) 정리 [링크](https://velog.io/@cmcm0012/%EB%A6%AC%EB%88%85%EC%8A%A4-Ch15.-The-Process-Address-Space)

- 240104 리눅스 cgroups(컨트롤 그룹) 학습
- 240109 연구 주제 세분화:

  1. NUMA 시스템에서의 도커 공유 메모리 성능 분석 -> 관련 논문 nuKSM 참고
  2. NUMA 시스템에서 Noisy Neighbor 문제에 의한 메모리 성능 저하 비교 분석 -> 특정 workload를 명시하여 분석한다면 좋을 것 같으나 cgroup, oom killer 등 다양한 방법으로 처리되고 있음

  Transparent Huge Page와 MGLRU에 대해 학습해보고 관련 주제로 작성 예정.

- 240117 MEMTIS 논문 확인

  Tiered Memory에 대해 다룬 MEMTIS 논문을 통해 MGLRU와는 어떻게 다른지 파악함.

- 240118 실험환경 설정 및 벤치마크

  MGLRU를 학습하고 해당 기능을 지원하는 리눅스 커널을 설치. MGLRU를 켜고 껐을 때의 메모리 활용 성능에 차이가 있는지 확인해보기 위해 XSBench를 이용, MGLRU 활성 여부에 따른 성능 차이 벤치마크. 현재까지는 성능차이 확인할 수 없어 벤치마크 파라미터 조정 및 다른 벤치마크 툴을 이용하여 추가적으로 분석이 필요할 것으로 보임.

-240125 탄소중립 키워드 포함

  carbond 논문 확인. Embodied emission과 Operational emission에 대해 관찰

-240131 

-240208 벤치마크 관련

  메모리 초기화 등 기본 작업 진행. 

-240216 ACT, carbond

  carbon footprint 계산을 위한 두개의 논문을 확인. ACT의 공개된 코드 확인. carbond의 공개된 코드 확인.