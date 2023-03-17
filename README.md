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

