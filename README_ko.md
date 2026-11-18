<div align="center">

# 정인호 · In Ho Jeung

Computer vision · 경량 모델 · 엣지 배포

동국대학교 석사과정 (2027년 8월 졸업 예정) · inislike [at] naver.com

[English](README.md) · 한국어

</div>

---

해상도가 낮거나 화질이 나쁜 영상에서도 잘 동작하는 경량 vision 모델(segmentation, detection, tracking)을 연구한다.
만든 모델은 Jetson Orin Nano, Android 폰, Raspberry Pi 5에 올려서 직접 측정한다.

## 연구

### EVWF-KD

저해상도에 노이즈까지 섞인 도로 영상의 semantic segmentation. 고해상도 영상과 pseudo-depth를 보는 teacher의 지식을,
저해상도 영상만 보는 3.7M 파라미터 student에 증류했다.

| 논문 | 속도 | 데이터셋 |
| :--- | :--- | :--- |
| Expert Systems with Applications, 제1저자 (심사 중) | Jetson Orin Nano 125 FPS, 스마트폰 59.4 FPS | CamVid, KITTI, MiniCity |

<p>
  <img src="https://img.shields.io/badge/Knowledge_Distillation-30363D?style=flat-square" />
  <img src="https://img.shields.io/badge/Semantic_Segmentation-30363D?style=flat-square" />
  <img src="https://img.shields.io/badge/Edge_AI-30363D?style=flat-square" />
</p>

[코드](https://github.com/NamsanMan/EVWF-KD)

## 프로젝트

<table>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/NamsanMan/edge-far-pedestrian-mot">
        <img src="https://raw.githubusercontent.com/NamsanMan/edge-far-pedestrian-mot/main/demo/dsec_clear_1.gif" width="100%" alt="멀리 있는 보행자 두 명, 기본 YOLOv8n과 YOLOv8n + S3x 비교" />
      </a>
      <h3>edge-far-pedestrian-mot</h3>
      <p>멀리 있어 폭이 몇 픽셀뿐인 보행자를 추적한다. YOLOv8n의 stride 네 곳을 바꿔 P3 격자를 가로로 두 배 촘촘하게
      만든 S3x를 제안했다(FLOPs +11 %). DSEC에서 파라미터가 3.8배인 YOLOv8s와 보행자 HOTA 차이가 0.4점 이내였고,
      Jetson Orin Nano에서 한 프레임 검출에 3.3 ms가 걸린다.</p>
      <p>
        <img src="https://img.shields.io/badge/YOLOv8-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/Multi--Object_Tracking-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/TensorRT-30363D?style=flat-square" />
      </p>
      <p><a href="https://github.com/NamsanMan/edge-far-pedestrian-mot">코드</a></p>
    </td>
    <td width="50%" valign="top">
      <a href="https://youtu.be/e3jIqR9ppsA">
        <img src="https://raw.githubusercontent.com/NamsanMan/edge-far-pedestrian-mot/main/apps/thermal_watch/media/thermal_watch_demo.jpg" width="100%" alt="Thermal Watch 데모 영상" />
      </a>
      <h3>Thermal Watch</h3>
      <p>S3x로 야간 열화상 드론 영상에서 사람을 찾는 앱을 만들었다. 드론 움직임을 보정해서 사람을 추적하고, 새 사람이
      나오면 사진과 거리를 붙여 경보를 띄운다. 학습에 안 쓴 녹화 영상에서 사람 AP50이 55.8에서 62.9로 올랐다.</p>
      <p>
        <img src="https://img.shields.io/badge/Thermal_Imaging-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/ByteTrack-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/HIT--UAV-30363D?style=flat-square" />
      </p>
      <p><a href="https://youtu.be/e3jIqR9ppsA">데모 영상</a> · <a href="https://github.com/NamsanMan/edge-far-pedestrian-mot/tree/main/apps/thermal_watch">코드</a></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <a href="https://github.com/NamsanMan/floor-vision-robot">
        <img src="https://raw.githubusercontent.com/NamsanMan/floor-vision-robot/main/media/git_01_lidar_vs_camera_stop.gif" width="100%" alt="LiDAR만 쓸 때와 카메라 바닥 분할을 쓸 때 비교" />
      </a>
      <h3>floor-vision-robot</h3>
      <p>2D LiDAR가 못 보는 낮은 장애물(책, 컵, 케이블)을 카메라 floor segmentation으로 찾아 Nav2에 넣었다. 연구에서
      만든 모델을 바닥 시점에 맞게 fine-tuning해서 Raspberry Pi 5 CPU에서 INT8로 돌렸다(한 장에 84 ms).</p>
      <p>
        <img src="https://img.shields.io/badge/ROS_2-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/Nav2-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/INT8-30363D?style=flat-square" />
      </p>
      <p><a href="https://github.com/NamsanMan/floor-vision-robot">코드</a></p>
    </td>
    <td width="50%" valign="top">
      <a href="https://github.com/NamsanMan/AI-HACK-CAMP-2026">
        <img src="https://raw.githubusercontent.com/NamsanMan/AI-HACK-CAMP-2026/main/docs/assets/overall_pipeline_korean.png" width="100%" alt="딥페이크 위험도 추정 파이프라인" />
      </a>
      <h3>딥페이크 위험도 추정</h3>
      <p>AI Hack Camp 2026 장려상. 화상통화 속 딥페이크를 잡는 모델로, 얼굴의 맥박 신호(rPPG)와 합성 흔적을 같이 본다.</p>
      <p>
        <img src="https://img.shields.io/badge/rPPG-30363D?style=flat-square" />
        <img src="https://img.shields.io/badge/Deepfake_Detection-30363D?style=flat-square" />
      </p>
      <p><a href="https://github.com/NamsanMan/AI-HACK-CAMP-2026">코드</a></p>
    </td>
  </tr>
</table>

## 논문

- EVWF-KD. Expert Systems with Applications, 제1저자, 심사 중.
- 차량 전방 카메라의 열화 저해상도 영상 시맨틱 분할을 위한 기존 연구 분석. 2026 대한전자공학회 추계학술대회.

## 활동

- AI Hack Camp 2026 장려상
- OSSCA, [파이토치 한국어 튜토리얼](https://github.com/PyTorchKR/tutorials-kr) 기여
- [Awesome-Physical-AI](https://github.com/PyTorchKR/Awesome-Physical-AI)(PyTorch KR) 기여, 세미나 발표

## 도구

| | |
| :--- | :--- |
| Vision·ML | Python, PyTorch, OpenCV, Ultralytics YOLO, Hugging Face Transformers |
| 엣지 배포 | TensorRT, ONNX Runtime, INT8 양자화, TFLite |
| 하드웨어 | Jetson Orin Nano, Raspberry Pi 5, Android |
| 로보틱스 | ROS 2, Nav2 |
| 기타 | Git, Docker, Linux |
