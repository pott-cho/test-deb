# test-deb

아주 간단한 테스트용 Debian 패키지 예제 레포입니다.

## 빌드 방식

Debian/Ubuntu 환경에서 필요한 패키지:

```bash
sudo apt-get update
sudo apt-get install -y autopkgtest build-essential debhelper devscripts
```

빌드:

```bash
dpkg-buildpackage -us -uc -b
```

성공하면 상위 디렉터리에 `hello-deb_0.1.0-1_all.deb` 같은 파일이 생성됩니다.

설치/실행:

```bash
sudo dpkg -i ../hello-deb_0.1.0-1_all.deb
hello-deb
```

삭제:

```bash
sudo dpkg -r hello-deb
```
