# Haking_Response
컴퓨터공학과 해킹과 대응기술 정리입니다.

[VMWARE Workstation Player 17 설치하기](https://www.vmware.com/content/vmware/vmware-published-sites/us/products/workstation-player/workstation-player-evaluation.html.html)
[VMWARE에 윈도우 XP 설치하기](https://blog.naver.com/nanisul2003/222998959523)
[VMWARE에 리눅스 칼리-1, 칼리-2 설치하기](https://digiconfactory.tistory.com/entry/VMWare-%EC%B9%BC%EB%A6%AC-%EB%A6%AC%EB%88%85%EC%8A%A4-%EB%B9%A0%EB%A5%B8%EC%84%A4%EC%B9%98)

![image](https://user-images.githubusercontent.com/58906858/223426082-c6a89aa0-7bab-46ad-a1fc-f453dbb37faa.png)   
![image](https://user-images.githubusercontent.com/58906858/223426176-dba95e31-4a95-4c9a-a921-ba901d615f17.png)   
![image](https://user-images.githubusercontent.com/58906858/223426215-46cc80be-57cb-47b0-8d18-9d1e08bfc344.png)

## VMware 실행
![image](https://user-images.githubusercontent.com/58906858/223436199-a408c363-344d-461f-980f-29df35830dba.png)   
![image](https://user-images.githubusercontent.com/58906858/223436311-4d346b10-09c1-4a8d-bb22-885b1c8f2228.png)   

## Windows XP 운영체제 설치

윈도우 XP iso파일을 넣어준다.
![image](https://user-images.githubusercontent.com/58906858/223436396-45008dcb-d6b9-4e1d-b014-7a083601ce77.png)

## 설치가 끝나면..
![image](https://user-images.githubusercontent.com/58906858/223443354-bf65fd12-876a-421f-9b36-31a88cc700e0.png)   
![image](https://user-images.githubusercontent.com/58906858/223444056-28bcaa88-77a3-4fe3-8455-76e8fb6b4201.png)      
![image](https://user-images.githubusercontent.com/58906858/223445783-d6e394a3-adb2-4f8d-a96a-dc493e453d59.png)

## VMware Windows XP에서 ip 확인하기

터미널에서 arp 명령어를 주면.. ip 주소를 확인할 수 있다..
![image](https://user-images.githubusercontent.com/58906858/223445349-c55ca46f-6cb9-42b2-9d81-f4d719e01033.png)

## 칼리 리눅스 설치하기

![image](https://user-images.githubusercontent.com/58906858/223458595-eb4ab9ec-cdc0-4c08-8f8e-4d10349de13a.png)

## 플립러닝2 (암호, 키 교환, 인증서) 2023-03-17
```
수신자의 공개키로 암호화(잠금)하는 행위는 기밀성을 확보한다.
송신자의 개인키로 암호화(잠금)하는 행위는 시그니처(전자서명), 인증, 부인방지, 무결성을 확보한다.
```
공개키 암호화와 전자서명의 차이는?
```
공개키 암호화에서 수신자의 공개키는 '평문을 암호화'하는 것이고 수신자의 개인키는 '암호문을 복호화'한다.

전자서명에서 송신자의 개인키는 '평문을 사용하여 서명'하기 위한 것이고, 
송신자의 공개키는 수신자가 '서명이 올바른지 검증'한다.
```

## Three way handshaking의 연결 과정을 그림으로 그리고 이해하라.
![image](https://user-images.githubusercontent.com/58906858/225877643-0aa6c0de-0d29-4ed8-a1e0-0f910284839a.png)
```
1. 클라이언트가 서버에게 연결을 요청합니다.
2. 서버는 요청을 받고 클라이언트에게 응답합니다.
3. 클라이언트는 서버의 응답을 받고 다시 응답합니다.
```

## Three way handshaking의 취약점을 이용한 공격 방법에 대해 조사하고 이해하라.
```
SYN Flood 공격
3-way handshaking에서 클라이언트가 SYN 패킷을 보내면 서버는 SYN-ACK 패킷으로 응답하고, 클라이언트는 ACK 패킷으로 응답하여 연결을 설정합니다. 
그러나, SYN Flood 공격을 통해 공격자가 대량의 SYN 패킷을 보내면 서버는 모든 연결 요청에 대한 SYN-ACK 패킷을 보내고 연결을 대기하는 상태가 됩니다. 
이로 인해 서버의 자원이 고갈되어 서비스가 마비될 수 있습니다.

IP Spoofing 공격
3-way handshaking에서는 클라이언트와 서버 간에 패킷 교환 시 시퀀스 번호와 확인 응답 번호를 사용하여 패킷의 순서를 확인합니다. 
그러나, IP Spoofing 공격을 통해 공격자가 위조된 IP 주소를 사용하여 패킷을 보낼 경우, 
클라이언트와 서버는 패킷의 순서를 확인할 수 없게 되어, 이를 이용한 공격이 가능해집니다.

중간자 공격
3-way handshaking에서는 클라이언트와 서버 간에 패킷 교환 시 암호화나 인증 과정이 없기 때문에, 중간자 공격에 취약합니다. 
공격자는 클라이언트와 서버 사이에서 패킷을 가로채어 내용을 확인하거나 수정할 수 있습니다.
이를 방지하기 위해서는 SSL/TLS와 같은 보안 프로토콜을 사용해야 합니다.
```

## 들어오는 패킷을 모두 거부하고, 192.168.0.33로부터 오는 패킷만을 허용하는 칼리 리눅스 명령어
```
iptables -P INPUT DROP
iptables -A INPUT -s 192.168.0.33 -j ACCEPT

위 명령어에서 첫 번째 줄은 들어오는 모든 패킷을 거부하도록 INPUT 체인의 기본 정책을 DROP으로 설정합니다. 
두 번째 줄은 192.168.0.33으로부터 오는 패킷을 수락하도록 INPUT 체인에 추가하는 명령어입니다.
-s 옵션은 송신지 IP 주소를 지정하는 옵션입니다. -j ACCEPT는 이 패킷을 수락하도록 설정하는 옵션입니다.

위 명령어를 실행하면 192.168.0.33에서 오는 패킷을 제외하고는 모든 패킷이 거부됩니다.
```

## tcp 프로토콜 패킷만을 거부하는 칼리 리눅스 명령어
```
iptables -A INPUT -p tcp -j DROP

위 명령어는 INPUT 체인에 대한 새 규칙을 추가합니다. 
-p tcp는 패킷 프로토콜이 TCP인 패킷만을 선택하고 -j DROP은 선택된 패킷을 버리도록 설정합니다.
따라서 이 명령어를 실행하면 TCP 패킷이 모두 거부됩니다.

-s 옵션으로 송신지 주소를 추가하는 부분을 수정해야합니다.
```

## Promiscuous mode 설정을 실습하고 과정을 설명하라.
```
ifconfig 명령어를 사용하여 인터페이스 이름을 확인합니다.
ifconfig

해당 인터페이스를 promiscuous mode로 설정합니다.
ifconfig [인터페이스 이름] promisc

예를 들어, eth0 인터페이스를 promiscuous mode로 설정하려면 다음 명령어를 실행합니다.
ifconfig eth0 promisc

promiscuous mode를 해제하려면 다음 명령어를 실행합니다.
ifconfig [인터페이스 이름] -promisc


예를 들어, eth0 인터페이스의 promiscuous mode를 해제하려면 다음 명령어를 실행합니다.
ifconfig eth0 -promisc

위의 명령어를 실행한 후, 해당 인터페이스는 모든 패킷을 수신할 수 있게 됩니다.
promiscuous mode는 보안 검사, 네트워크 모니터링, 패킷 분석 등에 유용하게 사용될 수 있지만, 
보안상의 이유로 일반적으로 사용하지 않는 것이 좋습니다.
```
