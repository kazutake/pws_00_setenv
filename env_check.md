# Anacondaの環境設定

# conda環境について

condaとpipは絶対に一緒にしない。


## 仮想環境の一覧を確認
```
>conda info -e
```

## 仮想環境をactivate(切り替え)
```
>source activate [env name]
or
>conda activate [env name]
```

## 現在の仮想環境から出る（deactivate)
```
>source deactivate
or
>conda deactivate
```

# 現在の仮想環境のパッケージ確認
```
>conda list
# packages in environment at C:\Users\riverlink\anaconda3:
#
# Name                    Version                   Build  Channel
_
zope                      1.0                      py38_1
zope.event                4.5.0                    py38_0
zope.interface            5.1.2            py38he774522_0
zstd                      1.4.5                h04227a9_0

  :
```

## conda を最新バージョンにする
```
>conda update conda	
```


## 更新
```
>conda update --all
or
>conda update [library name]
```

## condaパッケージ一覧の更新
```
>conda install -y conda-build
```

## 他のマシンで同じ環境を作る方法

### (1) 現在の仮想環境の設定を書き出す
```
>conda env export > env1.yaml
```

### (2)書き出した設定から仮想環境を作成する
```
>conda env create -f env1.yaml
```

### (3)既存環境をcloneという方法もある
```
>conda create --name riverlink --clone riverlink2
```


# 仮想環境を削除
```
>conda env remove -n riverlink
```

# gdal環境の構築
gdalが最新版のpythonに対応してない。Python3.5には対応している（2020.12.9現在）.
→　pythonのバージョンを指定して仮想環境を構築する
```
>conda create --name riverlink2 python=3.5 gdal
>conda activate gdalenv
```


# その他追加で入れたライブラリ

```
conda install -c anaconda netcdf4

conda install -c anaconda pyyaml

conda install -c anaconda pandas

conda install -c anaconda requests

conda install -c anaconda beautifulsoup4

conda install -c anaconda lxml

conda install -c anaconda numba

conda install -c anaconda h5py
```

以下参照

anaconda.org/anaconda/repo

