# ffplay 4.4


ffmpeg 4.4 のffplay を単独でコンパイルする環境をmesonで作成しました。

## 開発環境

- OS ：ubuntu 21.10、ビルドシステム：meson
- ffmpeg 4.4.1

## ビルド手順

```bash
sudo apt-get install ninja-build
sudo apt-get install meson

sudo apt-get install libavcodec-dev
sudo apt-get install libavformat-dev
sudo apt-get install libavfilter-dev
sudo apt-get install libavdevice-dev
sudo apt-get install libavresample-dev
sudo apt-get install -y libsdl2-dev libsdl2-image-dev libsdl2-mixer-dev libsdl2-net-dev libsdl2-ttf-dev

cd ../
git clone https://github.com/t-aikawa/ffplay_4_4-meson.git
cd ffplay_4_4-meson
./m

./builddir/ffplay -i ~/xxxxx.mp4
```
