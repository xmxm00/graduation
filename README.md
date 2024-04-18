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

- 240125 탄소중립 키워드 포함

  carbond 논문 확인. Embodied emission과 Operational emission에 대해 관찰

- 240208 MGLRU의 성능 분석을 위한 벤치마크

  메모리를 많이 활용하는 memtier-bench나 XSBench를 실행하였으나, 성능 변화를 찾지 못함.

- 240216 ACT, carbond

  Carbon footprint 계산을 위한 두개의 논문을 확인. Carbond에서의 계산법과 공개된 코드를 통해 carbond의 활용 방법에 대해 확인.

- 240221 Towards Application Centric Carbon Emission Management 논문 확인

  적은 성능 감소로 큰 폭의 탄소 배출량 감소효과를 확인할 수 있음. 일반적인 임계점이 있는지 분석해볼 수 있음.

- 240228 Carbond에서 Operational Carbon과 Embodied Carbon 출력

  rdtsc와 cpu cycle을 측정하고, powercap을 통해 전체 에너지를 측정. WattTime API를 통해 전력 생산에 발생하는 탄소 배출량을 확인하여 시스템에서 발생하는 탄소 배출량 확인.

- 240306 실험 환경 변경

  새로운 데스크탑에 리눅스 설치 및 원격 접속환경 설정, Carbond 구축 및 동작 확인.

- 240315 Carbond 코드 수정: Operational Carbon Emission 계산

  Carbond에서 Powercap 프레임워크를 활용해 package, core, dram의 에너지와 Operationcal carbon emission을 계산하고 CSV파일로 저장하도록 코드 수정

- 240322 Workload에 대한 Operational Carbon 계산

  Carbond에서 새로운 쓰레드를 통해 워크로드를 실행하여 그 때의 전력량을 측정할 수 있도록 Carbond 코드 수정.

- 240326 Freqmine, C-ray 벤치마크 진행

  CPU-intensive한 벤치마크인 Freqmine과 c-ray 벤치마크를 사용 가능한 코어 수를 제한해가며 실험. Freqmine의 데이터셋이 너무 작아 결과에 대한 경향성을 분석하기 어렵다 판단함.

- 240404 CPU와 DRAM의 Embodied Carbon 계산

  기존에는 워크로드를 수행하는 동안의 cpu cycle을 통해 Embodied Carbon을 계산하고자 하였으나, SCI 예제를 통해 계산식 수정.
  carbond에서 CPU와 DRAM의 사용량을 추적하고 이를 토대로 각각의 리소스에 대한 Embodied Carbon을 계산하여 저장하도록 구현.

- 240405 코어 수에 따른 단위 시간 당 에너지 사용량 분석

  c-ray 벤치마크에서는 4코어 이상 부터는 성능에 큰 차이가 없고, 소모하는 전력 역시 큰 차이를 보이지 않음.

- 240409 실험 환경 변경

  제온 E3를 이용하는 기존 환경에서는 코어 수가 부족한 등 경향성을 보기 어려운 문제가 있으므로 더 많은 물리 코어가 있는 다른 PC에서 실험 진행.
  변경된 PC에서 carbond가 올바른 리소스를 추적하도록 carbond 코드 수정.

- 240412 리소스 추적 기능 검증

  turbostat, perf와 같은 상용 툴과 비교하여 carbond가 올바르게 리소스 사용량을 추적하는지 교차검증.

- 240416 코어 에너지(pp0) 추적을 위한 커널 변경

  변경한 실험용 머신과 연구실 내 다른 워크스테이션에서 모두 코어에 대한 에너지를 측정할 수 없는 문제가 발생하여 커널 옵션 수정 후 빌드 테스트.

- 240417 소켓의 에너지 사용량을 토대로 분석

  CPU 레지스터에서 값이 0으로 고정되어 기능을 지원하지 않는 것을 확인. RAPL의 package가 소켓의 core와 uncore의 에너지 사용량을 대변하므로 해당 값을 이용해 실험 및 분석 진행.
