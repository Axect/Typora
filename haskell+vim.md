<h1 style="text-align:center">Haskell in Vim</h1>

<p style="text-align:right"><b>Tae Geun Kim</b></p>



## - Workflow 

* Tmux
* Haskell Vim Now
* Vim Slime



### 1) Tmux

* Tmux는 아주 좋은 Terminal Manager입니다. 아주 손 쉽게 터미널을 분할하고 각각의 터미널에 정보를 공유할 수 있습니다.

* 설치방법은 Tmux홈페이지를 참조하셔서 쉽게 따라하시면 됩니다.

* Tmux의 간단한 단축키는 다음과 같습니다.

  > Ctrl+B 를  Leader라고 하겠습니다.
  >
  > 1. Leader + " = 아래로 분할
  > 2. Leader + % = 우측으로 분할
  > 3. Leader + Arrow keys = 원하는 방향의 창으로 이동
  > 4. Leader + Ctrl + Arrow keys = 창 크기 조절



### 2) Haskell Vim Now

* 설치 및 단축키 모두 Haskell Vim Now Github를 참조하세요. 따라하시면 됩니다.
* Fedora 26 (Korora)의 경우 설치 종료과정에 에러가 나는데 큰 의미가 없습니다.
* 설치가 완료된 후 .vimrc는 이제 건드지 마세요. 플러그 추가는 .config/haskell-vim-now/plugins.vim 파일을 만들어서 Plug 커맨드를 이용하세요. 더불어 vim 설정도 그 파일에서 하면 쉽습니다.



### 3) Vim Slime

* 설치는 매우 쉽습니다. plugins.vim에 다음의 코드를 추가하세요.

  ```sh
  Plug 'jpalardy/vim-slime'

  let g:slime_target = "tmux"
  ```

* 단축키는 vim에서 C-c-c 입니다. (Ctrl+c+c)  창번호만 잘 입력하면 전송이 바로 됩니다. 창 번호는 tmux에서 Leader + q 로 알아낼 수 있습니다. 다 되었다면 한 pane에는 vim을 다른 pane에는 ghci를 켜서 잘 애용하시길 바랍니다.