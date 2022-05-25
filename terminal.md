zsh, git 설치

``` bash
sudo apt-get install zsh git
```

</br>

기본 쉘 변경 

``` bash
chsh -s $(which zsh)
```

</br>

oh-my-zsh 설치

``` bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 또는
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# 또는
sh -c "$(fetch -o - https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

</br>

power1evel10k 테마 설치

``` bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

</br>

zsh-syntax-highlighting 설치

``` bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
</br>

zsh-autosuggestions 설치
``` bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

</br>

테마 변경

``` bash
vim ~/.zshrc

...

if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
  source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
fi

...

ZSH_THEME="powerlevel10k/powerlevel10k"

...

plugins=(git
        zsh-syntax-highlighting
        zsh-autosuggestions)

...

[[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh
```

</br>

업데이트

``` bash
source ~/.zshrc
```

</br>
</br>
</br>

## wsl 한정 셋팅 

</br>

wsl 시작 시 자동 zsh 실행 

``` bash
nano ~/.bashrc


if [ -t 1 ]; then
exec zsh
fi
```