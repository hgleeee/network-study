# RDT (Reliable Data Transfer)

## 정의
- RDT는 신뢰성 있는 데이터 교환을 의미한다. 즉, 송/수신하는 데이터가 오류없이 온전히 전송되는 것을 뜻한다.
- Transport Layer(전송계층)에서는 신뢰성 있는 데이터 교환을 하고 싶어 하지만, 하위 레이어들에서는 신뢰성을 보장할 수 없기 때문에 문제가 발생할 수 있다. 
- 이를 해결하기 위해 Transport Layer에서 RDT 프로토콜을 이용할 수 있다.

## 데이터 송/수신 예시 (RDT 프로토콜 사용)

<p align="center"><img src="../images/ex_rdt_protocol.png" width="500"></p>

### 송신 측
- 상위 layer에서 보내려는 데이터가 있다면 rdt_send()를 호출해 데이터를 RDT 프로토콜로 전송한다.
- RDT 프로토콜에서 신뢰할 수 없는 채널인 하위 layer로 보낼 때 udt_send()를 호출해 패킷을 전송한다.
### 수신 측
- 하위 layer에서 받은 패킷이 있다면 rdt_rcv()를 호출해 RDT 프로토콜로 전송한다.
- RDT 프로토콜에서 상위 layer로 데이터를 보낼 때 deliver_data()를 호출해 데이터를 전송한다.

## FSM (Finite State Machines)

<p align="center"><img src="../images/fsm_model.png" width="500"></p>

- FSM이란 유한개의 상태(state)가 존재할 때, 어떠한 상태(state)가 어떠한 사건(event)에 의해 다른 상태(state)로 변하는 전이(transition)가 발생하는 것을 도식화한 모델이다. 
- 즉, event는 상태를 변화시키는 원인이고, actions는 상태가 변화할 때 취하는 행동을 말한다.


## rdt 1.0 (reliable transfer over a reliable channel)

## rdt 2.0 (channel with bit errors)

## rdt 2.0 (open with no errors, 에러가 없는 경우)

## rdt 2.0 (operaion with errors, 에러가 있는 경우)

## rdt 2.1

## rdt 2.2 (NAK-free protocol)

## rdt 3.0 (channels with errors and loss)
