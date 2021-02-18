#UBUNTU 18.04

apt install ffmpeg -y
apt install python3.7 -y
apt install python3.7-dev -y
apt install python3-pip -y
apt install unzip -y
apt install zlib1g.dev -y
apt install zlib1g -y
apt install libjpeg-dev -y
apt install libsm6 -y
apt install subversion -y

python3.7 -m pip install virtualenv
python3.7 -m pip install --upgrade pip wheel future-fstrings
#python3.7 -m pip install bpy --no-binary :all:
pip install bpy-2.91a0-cp37-cp37m-manylinux2014_x86_64.whl && bpy_post_install

curl 'https://psfiles.is.tuebingen.mpg.de/downloads/smpl/SMPL_unity_v-1-0-0-zip' -H 'User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:85.0) Gecko/20100101 Firefox/85.0' -H 'Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8' -H 'Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2' --compressed -H 'Connection: keep-alive' -H 'Referer: https://smpl.is.tue.mpg.de/downloads' -H 'Cookie: _ga=GA1.2.946776182.1587739197; _downlaods_manager_session=MWMwWlFDYnpVZ2FuWmNrNFM0M3Z3NjJZWXpZZlBHRnQwSVEzN0h0bFdaa2M2cjBCazM4QkFmUUIzWUNMTU5qR0lJUE9xM2JhRmh1MkErOFZNbkRCOFZ5cEgvRHlwQXMycmRWZTcxd2RqNWlSQlVjaFV0SjRlNEdZL2pwT0VSZjVMTW5oYktXZUZXRS9XS0c1M2JnNmVBPT0tLVZ6dkRrU2twMWVFRmJtRFFLNnppOEE9PQ%3D%3D--9a7f6434d5361de84b49dd22010c65a3710b4430' -H 'Upgrade-Insecure-Requests: 1' -k --output SMPL_unity_v.1.0.0.zip  


python lib/utils/fbx_output.py --input output/sample_video/vibe_output.pkl --output output/sample_video/fbx_output.fbx --fps_source 30 --fps_target 30     --gender female    --person_id 1