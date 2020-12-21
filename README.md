# deeplearning-danceschool
Learning to dance using Impersonator++!

Medium post & Video: https://kromme.medium.com/deep-learning-dance-school-97c5329b55b

![](https://miro.medium.com/max/700/1*WiWrMWB7uCzfwR9i83JyFQ.gif

I used the [Impersonator++](https://github.com/iPERDance/iPERCore) repo to map the movements of my GF's dancing video on a static picture of me. The following script was ran on Google Colab.

All Resources:
[![GitHub stars](https://img.shields.io/github/stars/iPERDance/iPERCore?style=social)](https://github.com/iPERDance/iPERCore)

- Paper: https://arxiv.org/pdf/2011.09055.pdf
- Repo: https://github.com/iPERDance/iPERCore
- Project Page: https://www.impersonator.org/work/impersonator-plus-plus.html
- Dataset https://svip-lab.github.io/dataset/iPER_dataset.html
- Forum https://discuss.impersonator.org/

## Note
Make sure that your runtime type is 'Python 3.6+ with GPU acceleration'. To do so, go to Edit > Notebook settings > Hardware Accelerator > Select "GPU".

## Dependencies
### System Requirements
 - Linux (test on Ubuntu 16.04 and 18.04) or Windows (test on windows 10)
 - CUDA 10.1, 10.2, or 11.0
 - gcc 7.5+ (needs to support C++14)
 - ffmpeg (ffprobe) 4.3.1+

### Python Requirements
- Python 3.6+
- PyTorch tested on 1.7.0
- Torchvison tested on 0.8.1
- mmcv-full test on 1.2.0
- numpy>=1.19.3
- scipy>=1.5.2
- scikit-image>=0.17.2
- opencv-python>=4.4.0.40
- tensorboardX>=2.1
- tqdm>=4.48.2
- visdom>=0.1.8.9
- easydict>=1.9
- toml>=0.10.2
- git+https://github.com/open-mmlab/mmdetection.git@8179440ec5f75fe95484854af61ce6f6279f3bbc
- git+https://github.com/open-mmlab/mmediting@d4086aaf8a36ae830f1714aad585900d24ad1156
- git+https://github.com/iPERDance/neural_renderer.git@e5f54f71a8941acf372514eb92e289872f272653

## Guidelines
### Source/Photo Guidelines:
- Try to capture the source images with the same static background without too complex scene structures. If possible, we recommend using the
actual background.
- The person in the source images holds an A-pose for introducing the most visible textures.
- It is recommended to capture the source images in an environment without too much contrast in lighting conditions and lock auto-exposure and auto-focus of the camera.

### Reference/Video Guidelines:
- Make sure that there is only **one** person in the reference video. Since,currently, our system does not support multiple people tracking. If there are multiple people, you need firstly use other video processing tools to crop the video.
- Make sure that capture the video with full body person. Half body will result in bad results.
- Try to capture the video with the static camera lens, and make sure that there is no too much zoom-in, zoom-out, panning, lens swichtings, and camera transitions. If there are multiple lens switchting and camera transitions, you need firstly use other video processing tools to crop the video.
