# 3D Reconstruction of Historical Landmarks with AR Deployment

A comprehensive computer vision project that reconstructs 3D models of historical landmarks from 2D images and deploys them in an Augmented Reality Android application.

## 🎬 Live Demo

![Live Recording](Reconstruction recording deployed.mp4)

## 👥 Authors

- **Jawad Saeed** - Department of Computer Science, LUMS  
  📧 25100094@lums.edu.pk

- **Ibrahim Farrukh** - Department of Computer Science, LUMS  
  📧 25100227@lums.edu.pk

## 🎯 Project Overview

This project implements an end-to-end pipeline for 3D reconstruction of historical landmarks using computer vision techniques, culminating in an AR-enabled Android application.

### 🏛️ Landmarks Reconstructed

- **Pantheon** (Primary focus)
- **Brandenburg Gate**

## 🚀 Features

- **Feature Detection & Matching**: SIFT-based feature extraction with robust matching
- **3D Reconstruction**: Structure from Motion (SfM) pipeline implementation
- **Point Cloud Generation**: Multi-view stereo techniques
- **Mesh Creation**: Poisson reconstruction for dense 3D meshes
- **AR Deployment**: Real-time visualization on Android devices
- **Cross-platform**: Flutter-based mobile application

## 📋 Project Components

### Environment Setup & Configuration

- Flutter installation and configuration
- Android Studio setup with SDK integration
- Device compatibility testing (Samsung Galaxy Note 8)
- Gradle version optimization for Java 21

### Basic 3D Reconstruction Pipeline

- Heritage Recon dataset preprocessing
- SIFT feature detection and visualization
- Brute-Force feature matching with cross-checking
- Camera pose estimation using fundamental/essential matrices
- Linear triangulation for 3D point generation

### Advanced Structure from Motion

- Multi-image dataset processing (Pantheon & Brandenburg Gate)
- Enhanced preprocessing with manual dataset cleaning
- Robust feature matching with Lowe's ratio test
- Global pose estimation and camera parameter extraction
- Dense point cloud generation and Poisson mesh reconstruction

### AR Application Development

- Integration with `ar_flutter_plugin`
- GLB file format conversion and optimization
- Local model loading and rendering
- Real-time AR visualization

## 🛠️ Technical Implementation

### Computer Vision Pipeline

```
Image Preprocessing → Feature Detection (SIFT) → Feature Matching (BF Matcher)
→ Camera Pose Estimation → 3D Triangulation → Point Cloud Generation
→ Mesh Reconstruction (Poisson) → Model Export (.ply/.glb)
```

### Key Algorithms Used

- **Scale-Invariant Feature Transform (SIFT)** for robust feature detection
- **Brute-Force Matcher** with L2 norm and cross-checking
- **RANSAC** for outlier filtering in fundamental matrix estimation
- **Lowe's Ratio Test** (threshold: 0.7) for high-quality matches
- **Poisson Reconstruction** for dense mesh generation

### Technologies & Libraries

- **Flutter** - Cross-platform mobile development
- **OpenCV** - Computer vision operations
- **Open3D** - 3D data processing and visualization
- **ar_flutter_plugin** - Augmented Reality integration
- **Python** - Core reconstruction pipeline
- **Android Studio** - Mobile development environment

## 📱 Mobile Application Features

- Real-time camera integration
- Local 3D model loading
- Interactive AR visualization
- Touch controls for model manipulation
- Optimized rendering for mobile hardware

## 🎥 Demo & Results

### Visual Outputs

- **Feature Extraction**: SIFT keypoints visualization
- **Feature Matching**: Correspondence mapping between image pairs
- **3D Point Clouds**: Sparse reconstruction results
- **3D Meshes**: Dense reconstructed models
- **AR Deployment**: Live camera integration with 3D models

### Performance Metrics

- **Feature Detection**: Up to 5,000 features per image
- **Feature Matching**: Top 100 matches retained per image pair
- **Image Resolution**: Standardized to 800×600 pixels
- **Reconstruction Quality**: Varies by dataset continuity and image quality

## 📊 Results & Findings

### Brandenburg Gate Reconstruction

- ✅ Overall geometric structure captured successfully
- ⚠️ Partial reconstruction with some displaced pillars
- ❌ Missing intricate details (horses atop the gate)
- 🔍 Issues caused by people interference and inconsistent angles

### Pantheon Reconstruction

- ✅ Architectural elements like pediment and pillars visible
- ⚠️ Significant distortions due to dataset discontinuity
- ❌ High human presence in images affected pose estimation
- 🔧 Requires dataset refinement for improved results

### AR Deployment

- ✅ Successful model loading and visualization
- ✅ Real-time camera integration working
- ⚠️ Performance limited by hardware capabilities
- 🔋 GPU memory constraints on older devices

## 🔧 Installation & Setup

### Prerequisites

- Flutter SDK (latest stable version)
- Android Studio Ladybug with Android SDK
- Python 3.8+ with required packages
- Android device with ARCore support (recommended)

### Flutter Dependencies

```yaml
dependencies:
  flutter:
    sdk: flutter
  ar_flutter_plugin: ^0.7.3
  # Additional dependencies as specified in pubspec.yaml
```

### Python Dependencies

```bash
pip install opencv-python numpy open3d matplotlib
```

### Setup Instructions

1. Clone the repository
2. Install Flutter and verify with `flutter doctor`
3. Connect Android device with USB debugging enabled
4. Run `flutter pub get` to install dependencies
5. Execute `flutter run` to deploy the application

## 📁 File Structure

```

├── assets/models/           # 3D model files (.glb, .ply)
├── notebooks/              # Jupyter notebooks for reconstruction pipeline
├── results/                   # Project documentation and report
└── recordings/             # Demo videos and visualizations
```

## 🚧 Known Issues & Limitations

### Technical Challenges

- **Dataset Quality**: Inconsistent image sequences affect reconstruction quality
- **Hardware Constraints**: Limited GPU memory on older Android devices
- **Library Compatibility**: Outdated AR libraries requiring manual modifications
- **File Format Conversion**: Lossy .ply to .glb conversion issues

### Reconstruction Limitations

- Incomplete architectural details in complex structures
- Sensitivity to human presence in images
- Requires careful dataset preprocessing and cleaning
- Performance varies significantly with image continuity

## 🔮 Future Improvements

### Technical Enhancements

- **Advanced Algorithms**: Implement deep learning-based feature matching
- **Dataset Optimization**: Automated image filtering and sequence optimization
- **Performance**: GPU acceleration for mobile rendering
- **Accuracy**: Bundle adjustment for improved camera pose estimation

### Application Features

- **Multi-model Support**: Load and switch between different landmarks
- **Interactive Controls**: Enhanced AR manipulation and scaling
- **Cloud Integration**: Remote model loading and sharing
- **Educational Content**: Historical information overlay

## 📚 References & Resources

- Heritage Recon Dataset
- OpenCV Documentation
- Open3D Library Documentation
- Flutter AR Plugin Documentation
- Structure from Motion Literature

## 📄 License

This project is developed for educational and research purposes.

## 🤝 Contributing

For questions or collaboration inquiries, please contact the authors directly.

---

**Built with passion for Computer Vision and Augmented Reality**
