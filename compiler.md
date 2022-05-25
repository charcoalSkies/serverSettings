gcc, g++ 설치

``` bash
sudo apt-get update

sudo apt-get install build-essential

gcc --version && g++ --version
```

</br>

rsut 설치

``` bash
curl https://sh.rustup.rs -sSf | sh

source $HOME/.cargo/env

export PATH="$HOME/.cargo/bin:$PATH"

rustup update

rustc --version

```

</br>

python 3.9.x

``` bash
sudo apt update

sudo apt install software-properties-common

# 저장소를 추가 한 후 Ubuntu 20.04에서는 사용 가능한 패키지 목록이 업데이트됩니다.. 저장소가 활성화되고 모든 것이 업데이트되면 다음 단계로 진행할 수 있습니다.
sudo add-apt-repository ppa:deadsnakes/ppa

sudo apt install python3.9

sudo apt update && sudo apt install python3-pip
```
