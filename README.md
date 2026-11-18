<div align="center">

# In Ho Jeung

Computer vision · lightweight models · edge deployment

M.S. student, Dongguk University · graduating Aug 2027

<a href="mailto:inislike@naver.com"><img src="https://img.shields.io/badge/inislike%40naver.com-30363D?style=flat-square&logo=naver&logoColor=white" alt="Email" /></a>

English · [한국어](README_ko.md)

</div>

---

I work on lightweight vision models (segmentation, detection, tracking) for low-resolution and low-quality images.
I deploy them and measure them on a Jetson Orin Nano, an Android phone and a Raspberry Pi 5.

## Research

### EVWF-KD

Semantic segmentation of noisy, low-resolution road images. A teacher that sees the high-resolution image and a
pseudo-depth map is distilled into a 3.7M-parameter student that sees only the low-resolution image.

| Paper | Speed | Datasets |
| :--- | :--- | :--- |
| Expert Systems with Applications, first author (under review) | 125 FPS on Jetson Orin Nano, 59.4 FPS on a phone | CamVid, KITTI, MiniCity |

<p>
  <img src="https://img.shields.io/badge/Knowledge_Distillation-30363D?style=flat-square" />
  <img src="https://img.shields.io/badge/Semantic_Segmentation-30363D?style=flat-square" />
  <img src="https://img.shields.io/badge/Edge_AI-30363D?style=flat-square" />
</p>

[Code](https://github.com/NamsanMan/EVWF-KD)

## Projects

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/NamsanMan/edge-far-pedestrian-mot">
        <img src="https://raw.githubusercontent.com/NamsanMan/edge-far-pedestrian-mot/main/demo/dsec_clear_1.gif" width="100%" alt="Plain YOLOv8n vs YOLOv8n + S3x on two far pedestrians" />
      </a>
      <h3>edge-far-pedestrian-mot</h3>
      <p>Tracking far pedestrians that are only a few pixels wide. I proposed S3x, which changes four strides in YOLOv8n so
      its P3 grid is twice as fine horizontally (+11 % FLOPs). On DSEC its pedestrian HOTA is within 0.4 points of
      YOLOv8s, which has 3.8 times the parameters. The detector takes 3.3 ms on a Jetson Orin Nano.</p>
      <p>
        <img src="https://img.shields.io/badge/YOLOv8-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/Multi--Object_Tracking-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/TensorRT-30363D?style=flat-square" />
      </p>
      <p><a href="https://github.com/NamsanMan/edge-far-pedestrian-mot">Code</a></p>
    </td>
    <td width="50%" valign="top">
      <a href="https://youtu.be/e3jIqR9ppsA">
        <img src="https://raw.githubusercontent.com/NamsanMan/edge-far-pedestrian-mot/main/apps/thermal_watch/media/thermal_watch_demo.jpg" width="100%" alt="Thermal Watch demo video" />
      </a>
      <h3>Thermal Watch</h3>
      <p>An app that finds people in night thermal drone video with S3x. It compensates the drone's motion, tracks people
      and raises an alert with a snapshot and the distance for each new person. Person AP50 on recordings not used in
      training went from 55.8 to 62.9.</p>
      <p>
        <img src="https://img.shields.io/badge/Thermal_Imaging-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/ByteTrack-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/HIT--UAV-30363D?style=flat-square" />
      </p>
      <p><a href="https://youtu.be/e3jIqR9ppsA">Demo video</a> · <a href="https://github.com/NamsanMan/edge-far-pedestrian-mot/tree/main/apps/thermal_watch">Code</a></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/NamsanMan/floor-vision-robot">
        <img src="https://raw.githubusercontent.com/NamsanMan/floor-vision-robot/main/media/git_01_lidar_vs_camera_stop.gif" width="100%" alt="LiDAR only vs camera floor segmentation" />
      </a>
      <h3>floor-vision-robot</h3>
      <p>A Raspberry Pi 5 robot that stops before low obstacles (books, cups, cables) its 2D LiDAR cannot see. My
      segmentation model, fine-tuned to segment the floor, runs in INT8 on the Pi CPU (84 ms per frame) and feeds the
      obstacles to Nav2.</p>
      <p>
        <img src="https://img.shields.io/badge/ROS_2-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/Nav2-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/INT8-30363D?style=flat-square" />
      </p>
      <p><a href="https://github.com/NamsanMan/floor-vision-robot">Code</a></p>
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/NamsanMan/AI-HACK-CAMP-2026">
        <img src="https://raw.githubusercontent.com/NamsanMan/AI-HACK-CAMP-2026/main/docs/assets/overall_pipeline_korean.png" width="100%" alt="Deepfake risk estimation pipeline" />
      </a>
      <h3>Deepfake risk estimation</h3>
      <p>Encouragement Award, AI Hack Camp 2026. Deepfake detection for video calls that combines the pulse signal of
      the face (rPPG) with synthesis artifacts.</p>
      <p>
        <img src="https://img.shields.io/badge/rPPG-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/Deepfake_Detection-30363D?style=flat-square" />
      </p>
      <p><a href="https://github.com/NamsanMan/AI-HACK-CAMP-2026">Code</a></p>
    </td>
  </tr>
</table>

## Papers

- EVWF-KD. Expert Systems with Applications, first author, under review.
- A Review on Semantic Segmentation of Degraded Low-resolution Images from Vehicle-mounted Front-facing Cameras.
  IEIE Fall Conference 2026.

## Activities

- AI Hack Camp 2026, Encouragement Award
- OSSCA, contributor to the [PyTorch Korean tutorials](https://github.com/PyTorchKR/tutorials-kr)
- [Awesome-Physical-AI](https://github.com/PyTorchKR/Awesome-Physical-AI) (PyTorch KR), contributor and seminar speaker

## Tools

| | |
| :--- | :--- |
| Vision and ML | Python, PyTorch, OpenCV, Ultralytics YOLO, Hugging Face Transformers |
| Edge deployment | TensorRT, ONNX Runtime, INT8 quantization, TFLite |
| Hardware | Jetson Orin Nano, Raspberry Pi 5, Android |
| Robotics | ROS 2, Nav2 |
| Other | Git, Docker, Linux |

## Coding test

<a href="https://github.com/NamsanMan/Programmers"><img src="https://img.shields.io/github/directory-file-count/NamsanMan/Programmers/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%A8%B8%EC%8A%A4%2F1?type=dir&label=Programmers%20Lv.1&style=flat-square&labelColor=30363D&color=4C5866" alt="Programmers Lv.1" /></a>
<a href="https://github.com/NamsanMan/Programmers"><img src="https://img.shields.io/github/directory-file-count/NamsanMan/Programmers/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%A8%B8%EC%8A%A4%2F2?type=dir&label=Programmers%20Lv.2&style=flat-square&labelColor=30363D&color=4C5866" alt="Programmers Lv.2" /></a>
<a href="https://github.com/NamsanMan/Programmers"><img src="https://img.shields.io/github/directory-file-count/NamsanMan/Programmers/%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%A8%B8%EC%8A%A4%2F3?type=dir&label=Programmers%20Lv.3&style=flat-square&labelColor=30363D&color=4C5866" alt="Programmers Lv.3" /></a>
