## 拉取镜像
```
docker run -itd \
    --name mt798x-build \
    -v /you_code_dir:/work \
    ubuntu:22.04
```

## 进入容器
```
docker exec -it mt798x-build /bin/bash
```

## 安装依赖
```
apt install gcc-aarch64-linux-gnu build-essential flex bison libssl-dev device-tree-compiler qemu-user-static
```

## 工作目录
```
cd /work
```

## 编译
```
SOC=mt7981 BOARD=cmcc_mr3000d-cig ./build.sh
```