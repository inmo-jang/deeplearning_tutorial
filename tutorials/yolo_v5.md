# What to know in using Yolo v5

## (1) Using PyTorch GPU version is much faster

Although it is actually very obvious, I tried to test how faster using PyTorch GPU version would be by myself. 

To get this test done very simply, I used an `ipynb` file that include some commands as follows:

```
import torch

print(f"Setup complete. Using torch {torch.__version__} ({torch.cuda.get_device_properties(0).name if torch.cuda.is_available() else 'CPU'})")

!python detect.py --source 0
```

The second line will tell you which version of torch is activated. 

The third line needs a webcam on your PC, and will show a camera view and do a real-time object detection process. 

My GPU option was as follows, and I felt that the object detection process was successfuly done in real time.  
```
Using torch 1.8.2+cu111 (NVIDIA GeForce RTX 2070 Super with Max-Q Design)
```

My CPU option was as follows, but compared to the above, the process was so slower even on my laptop. (I felt like it was around 2 FPS) 
```
Using torch 1.8.2 (CPU)
```


Click the following image to see the comparison test video:
[![Video Label](https://img.youtube.com/vi/n8Ef54HfWhw/0.jpg)](https://youtu.be/n8Ef54HfWhw) 
