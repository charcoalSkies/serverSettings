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

이전버전 파이썬 삭제 

``` bash
whereis python

x.x

sudo apt-get update

rm -rf /usr/lib/pythonx.x

rm -rf /etc/pythonx.x
```

</br>

파이썬 설치 python x.x

``` bash
sudo apt update

sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev

wget https://www.python.org/ftp/python/3.9.13/Python-3.9.13.tgz

tar -xf Python-3.9.13.tgz

cd Python-3.9.13

./configure --enable-optimizations

make -j 12

sudo make altinstall

python3.9 -V

pip3.9 -V

/usr/local/bin/python3.9 -m pip install --upgrade pip
```



