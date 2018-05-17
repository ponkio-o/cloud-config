# cloud-config
CoreOSインストール時の設定ファイル

## Setup
`[username]` 任意のユーザー名

`[password_hash]` ハッシュ値

```bash
$ mkpasswd -m sha-512 password
$6$ne2nNyN5b.r/D0$kfyVXjhPeLCuCvwUVoOV1fmvXj7pDqSO1n2Gy/PcFHO2SCR2OXQwA0Cb3YWQOD2P8kiA1gL/OHX1tFkuAS.Nk/
```

## Install
```bash
$ sudo coreos-install -d /dev/vda -c stable -c cloud-config.yml
```

## Settings
```bash
$ sudo vim /var/lib/coreos-install/user_data
$ sudo reboot
```
