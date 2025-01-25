
### CUDA Tollkit 12.6
``

```
wget https://developer.download.nvidia.com/compute/cuda/12.6.3/local_installers/cuda_12.6.3_560.35.05_linux.run
```

```
sudo sh cuda_12.6.3_560.35.05_linux.run
```

```
nano ~/.zshrc
```

```
export PATH=/usr/local/cuda-12.6/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda-12.6/lib64:$LD_LIBRARY_PATH
```

```
source ~/.bashrc   # or source ~/.zshrc
```

```
nvcc --version
```


### cuDNN 9.6

```
wget https://developer.download.nvidia.com/compute/cudnn/redist/cudnn/linux-x86_64/cudnn-linux-x86_64-9.6.0.74_cuda12-archive.tar.xz
```

```
tar -xvf cudnn-linux-x86_64-9.6.0.74_cuda12-archive.tar.xz
```

```
sudo cp cudnn-linux-x86_64-9.6.0.74_cuda12-archive/include/cudnn*.h /usr/local/cuda-12.6/include
```

```
sudo cp cudnn-linux-x86_64-9.6.0.74_cuda12-archive/lib/libcudnn* /usr/local/cuda-12.6/lib64
```

```
cat /usr/local/cuda-12.6/include/cudnn_version.h | grep CUDNN_MAJOR -A 2
```


### TensorRT 10.7 GA

```
wget https://developer.nvidia.com/downloads/compute/machine-learning/tensorrt/10.7.0/tars/TensorRT-10.7.0.23.Linux.x86_64-gnu.cuda-12.6.tar.gz
```

```
tar -xvf TensorRT-10.7.0.23.Linux.x86_64-gnu.cuda-12.6.tar.gz
```

```
sudo cp -r TensorRT-10.7.0.23/include/* /usr/local/cuda-12.6/include/
```

```
sudo cp -r TensorRT-10.7.0.23/lib/* /usr/local/cuda-12.6/lib64/
```

```
ls /usr/local/cuda-12.6/lib64 | grep nvinfer
```



### ipykernel

```
pip install ipykernel
```

```
python -m ipykernel install --user --name=tensor --display-name "Tensor"
```

