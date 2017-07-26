# haar-like cascade detectorで顔認識

大阪Pythonの会#04のハンズオン資料

opencvに予め用意されている分類器で人の顔を検出していきます。

## Anacondaで環境構築

※Macを使用しているので、windows環境は動作確認できていません。

### windows

インストーラーでAnacondaを導入します。https://www.continuum.io/downloads

```
conda create -n haarcascade_env python=3.5 jupyter numpy matplotlib
activate haarcascade_env
conda install -c https://conda.anaconda.org/menpo opencv3
jupyter notebook
```

### mac

まずpyenv(anyenv)を経由してインストールします。未導入の方はこちらから[anyenvで開発環境を整える](http://qiita.com/luckypool/items/f1e756e9d3e9786ad9ea)

```
pyenv install anaconda3-4.3.0
pyenv local anaconda3-4.3.0

conda create -n haarcascade_env python=3.5 jupyter numpy matplotlib
```

cond info -eで表示されるrootのパス末尾に"/bin/activate"を追加して、エイリアスを作成します。

```
conda info -e
 haarcascade_env          /Users/(user_name)/.anyenv/envs/pyenv/versions/anaconda3-4.3.0/envs/haarcascade_env
 root                  *  /Users/(user_name)/.anyenv/envs/pyenv/versions/anaconda3-4.3.0

echo "alias activate='source /Users/(user_name)/.anyenv/envs/pyenv/versions/anaconda3-4.3.0/bin/activate'" >> ~/.bashrc
source ~/.bashrc
echo "source ~/.bashrc" >> ~/.bash_profile #毎回 source ~/.bashrcが面倒なら実行
```

```
activate haarcascade_env
conda install -c https://conda.anaconda.org/menpo opencv3
jupyter notebook
```
