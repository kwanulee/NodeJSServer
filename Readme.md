# AWS에서 실행 방법
## 1. 사전준비
1. [키페어 생성하기](./doc/create_keypair.pdf)
1. [보안그룹 생성하기](./doc/create_security_group.pdf)
2. [**AWS**에서 (Linux) 인스턴스 시작](./doc/launch_instance.md)
3. [(Linux) 인스턴스 연결](./doc/connectingToInstance.pdf)

## 2. NodeJS 설치
Package Manager를 통한 NodeJS 설치

- https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-basedlinux-distributions
참조

```
[ubuntu ~]$ curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
```

```
[ubuntu ~]$ sudo apt-get install -y nodejs
```
## 3. MongDB 설치
Install MongoDB Community Edition on Ubuntu

- https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/

1. Import the public key used by the package management system.

	```
	[ubuntu ~]$ sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 0C49F3730359A14518585931BC711F9BA15703C6
	```

2. Create a list file for MongoDB.

	Ubuntu 16.04

	```
	[ubuntu ~]$ echo "deb [ arch=amd64,arm64 ] http://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/3.4 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.4.list
	```
	
3. Reload local package database.

	```
	[ubuntu ~]$ sudo apt-get update
	```
	
4. Install the MongoDB packages.

	```
	[ubuntu ~]$ sudo apt-get install -y mongodb-org
	```

5. Start MongoDB.
6. 
	```
	[ubuntu ~]$ sudo service mongod start
	```

## 4. APP 다운로드 및 실행
1. GitHub 저장소에서 App 다운로드

	```
	[ubuntu ~]$ git clone https://github.com/kwanulee/NodeJSServer
	```

2. App 폴더로 이동

	```
	[ubuntu ~]$ cd NodeJSServer
	```

3. App 실행

	```
	[ubuntu ~]$ sudo node app.js&
	```

4. 서버가 정상적으로 실행되면, https://github.com/kwanulee/AndroidNodeJS 안드로이드 프로젝트를 다운받아 디바이스에 설치하고 실행해 본다.
