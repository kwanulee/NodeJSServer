# **AWS**에서 (Linux) 인스턴스 시작

1. https://console.aws.amazon.com/ec2/ 에서 Amazon EC2 콘솔을 엽니다.
2. 콘솔 대시보드에서 **[Launch Instance]**를 선택합니다.
	+ **[Choose an Amazon Machine Image (AMI)]** 페이지에 인스턴스에 대한 템플릿 역할을 하는 **[Amazon Machine Images (AMIs)]**라는 기본 구성 목록이 표시
3. **Ubuntu Server 16.04 LTS (HVM), SSD Volume Type** 버전을 선택
4. **[Choose an Instance Type]** 페이지에서 인스턴스의 하드웨어 구성을 선택할 수 있습니다. 기본적으로 선택된 **t2.micro** 유형을 선택
5. **[Review and Launch]**를 선택하여 마법사가 다른 구성 설정을 완료
6. **[Review Instance Launch]** 페이지의 보안 그룹을 사용하거나, 설정을 시작할때 만든 보안 그룹을 선택
	1. **[Edit security groups]**를 선택합니다.
	2. **[Configure Security Group]** 페이지에서 **[Select an existing security group]**이 선택되어 있는지 확인합니다.
	3. 기존 보안 그룹 목록에서 보안 그룹을 선택한 다음 **[Review and Launch]**를 선택
7. **[Review Instance Launch]** 페이지에서 **[Launch]**를 선택
8. 키 페어에 대한 메시지가 나타나면 **[Choose an existing key pair]**를 선택한 다음 설치할 때 생성한 키 페어를 선택
9. 승인 확인란을 체크한 다음 **[Launch Instances]**를 선택
10. **[View Instances]**를 선택하여, **[Instances]** 화면에서 시작 상태를 볼 수 있음
11. 연결할 수 있도록 인스턴스가 준비될 때까지 몇 분 정도 걸릴 수 있습니
다. 인스턴스가 상태 확인을 통과했는지 확인하십시오. **[Status Checks]**
열에서 이 정보를 볼 수 있습니다.

