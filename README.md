# Event-based Vision References

## Sorted by topic:
- [Devices](#devices)
- [Neuromorphic Systems](#neuromorphic-systems)
- [Drivers](#drivers)
- [Calibration](#calibration)
- Algorithms:
    - [Feature detection and Tracking](#feature-detection)
    - [Depth estimation (3D Reconstruction)](#depth-estimation)
    	- [Monocular](#depth-mono)
    	- [Stereo](#depth-stereo)
    - [Optical flow](#optical-flow)
    - [Intensity-Image reconstruction](#image-reconstruction)
    - [Localization and Ego-motion estimation](#egomotion)
    - [Visual Odometry and SLAM (Simultaneous Localization And Mapping)](#VOSLAM)
    - [Visual-Inertial Odometry](#visual-inertial)
    - Pattern recognition
        - Gesture control
        - Classification:
    	- Object detection:
    	- Neural Networks:
    - Signal Processing
    - Controllers

- [Datasets and simulators](#datasets)

- [Workshops](#workshops)

- People / Research Groups


<a name="devices"></a>
## Devices
- **DVS (Dynamic Vision Sensor)**: Lichtsteiner, P., Posch, C., and Delbruck, T., *[A 128x128 120dB 15μs latency asynchronous temporal contrast vision sensor](http://doi.org/10.1109/JSSC.2007.914337)*, IEEE J. Solid-State Circuits, 43(2):566--576, 2008.
    - [Product page at iniLabs](https://inilabs.com/products/dynamic-vision-sensors/)
    - [Introductory videos about the DVS](https://inilabs.com/videos/dvs-introduction/)
- **DAVIS (Dynamic and Active-Pixel Vision Sensor)** :
Brandli, C., Berner, R., Yang, M., Liu, S.-C., Delbruck, T., *[A 240x180 130 dB 3 µs Latency Global Shutter Spatiotemporal Vision Sensor](https://doi.org/10.1109/JSSC.2014.2342715)*, IEEE J. Solid-State Circuits, 49(10):2333--2341, 2014.
    - [Product page at iniLabs](https://inilabs.com/products/dynamic-and-active-pixel-vision-sensor/)
    - **Color-DAVIS**: Li, C., Brandli, C., Berner, R., Liu, H., Yang, M., Liu, S.-C., Delbruck, T., [Design of an RGBW Color VGA Rolling and Global Shutter Dynamic and Active-Pixel Vision Sensor](https://doi.org/10.1109/ISCAS.2015.7168734), IEEE Int. Symp. Circuits and Systems (ISCAS), Lisbon, 2015, pp. 718--721.

- **ATIS (Asynchronous Time-based Image Sensor)**: Posch, C., Matolin, D., Wohlgenannt, R. (2011). *[A QVGA 143 dB Dynamic Range Frame-Free PWM Image Sensor With Lossless Pixel-Level Video Compression and Time-Domain CDS](http://doi.org/10.1109/JSSC.2010.2085952)*, IEEE J. Solid-State Circuits, 46(1):259--275, 2011.
    - [Chronocam](http://www.chronocam.com/)
- Samsung's DVS (Gen2). [Yoel Yaffe](https://www.linkedin.com/in/yoel-yaffe-a606841/), Samsung Israel Research Center, Samsung Electronics.
- CeleX ([Hillhouse Technology](http://www.hillhouse-tech.com/), Singapore). [YouTube](https://youtu.be/Wlzc-5sgm1g)
- [Insightness AG](http://www.insightness.com/). [The Silicon Eye](http://www.insightness.com/?p=361) Technology

<a name="neuromorphic-systems"></a>
## Neuromorphic Systems
- Liu, S.-C. and Delbruck, T., [Neuromorphic sensory systems](https://doi.org/10.1016/j.conb.2010.03.007), Current Opinion in Neurobiology, 20:3(288--295), 2010.
- Liu, S.-C., Delbruck, T., Indiveri, G., Whatley, A., Douglas, R., [Event-Based Neuromorphic Systems](http://eu.wiley.com/WileyCDA/WileyTitle/productCd-1118927621.html), Wiley. ISBN: 978-1-118-92762-5, 2014.

<a name="drivers"></a>
## Drivers
- [jAER (java Address-Event Representation) project](http://jaerproject.org/)
- [caer (AER event-based framework, written in C, targeting embedded systems)](https://github.com/inilabs/caer)
- [libcaer (Minimal C library to access, configure and get/send AER data from sensors or to/from neuromorphic processors)](https://github.com/inilabs/libcaer)
- [ROS (Robotic Operating System)](https://github.com/uzh-rpg/rpg_dvs_ros)


<a name="calibration"></a>
## Calibration
- For the DAVIS: use the grayscale frames, with standard software such as ROS camera calibrator, kalibr, ...
- For the DAVIS camera and IMU calibration: kalibr.
- For the DVS (events-only):
    - [Calibration using blinking LEDs or computer screens](https://github.com/uzh-rpg/rpg_dvs_ros/tree/master/dvs_calibration) from RPG - UZH.
    - [DVS camera calibration](https://github.com/VLOGroup/dvs-calibration) from VLOGroup at TU Graz, Austria.


# Algorithms

<a name="feature-detection"></a>
## Feature Detection and Tracking
- Tedaldi, D., Gallego, G., Mueggler, E., Scaramuzza, D., [Feature detection and tracking with the dynamic and active-pixel vision sensor (DAVIS)](https://doi.org/10.1109/EBCCSP.2016.7605086), IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Tedaldi.pdf), [YouTube](https://www.youtube.com/watch?v=nglfEkiK308)
- Braendli, C., Strubel, J., Keller, S., Scaramuzza, D., Delbruck, T., [ELiSeD - An Event-Based Line Segment Detector](https://doi.org/10.1109/EBCCSP.2016.7605244) Int. Conf. on Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/EBCCSP16_Braendli.pdf)
- Zhu, A., Atanasov, N., Daniilidis, K., [Event-based Feature Tracking with Probabilistic Data Associations](https://fling.seas.upenn.edu/~alexzhu/dynamic/event-based-feature-tracking-with-probabilistic-data-association/), IEEE Int. Conf. Robotics and Automation (ICRA), Singapore, 2017. [YouTube](https://youtu.be/m93XCqAS6Fc)


<a name="depth-estimation"></a>
## Depth Estimation (3D Reconstruction)

<a name="depth-mono"></a>
### Monocular Depth Estimation
- Rebecq, H., Gallego, G., Scaramuzza, D., [EMVS: Event-based Multi-View Stereo](http://www.bmva.org/bmvc/2016/papers/paper063/), British Machine Vision Conference (BMVC), York, 2016. [PDF](http://rpg.ifi.uzh.ch/docs/BMVC16_Rebecq.pdf), [YouTube](https://www.youtube.com/watch?v=EUX3Tfx0KKE), [3D Reconstruction Experiments from a Train using an Event Camera](https://www.youtube.com/watch?v=fA4MiSzYHWA)

### Monocular Depth Estimation using Structured Light
- Brandli, C., Mantel, T.A., Hutter, M., Hoepflinger, M.A., Berner, R., Siegwart, R., Delbruck, T., [Adaptive Pulsed Laser Line Extraction for Terrain Reconstruction using a Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00275). Front. Neurosci. (2014) 7:275. [PDF](http://www.zora.uzh.ch/107736/1/fnins-07-00275.pdf), [YouTube](https://youtu.be/20OGD5Wwe9Q)
- Matsuda, N., Cossairt, O., Gupta, M., [MC3D: Motion Contrast 3D Scanning](https://doi.org/10.1109/ICCPHOT.2015.7168370), IEEE Conf. Computational Photography (ICCP), Houston,TX, 2015, pp. 1-10. [PDF](http://compphotolab.northwestern.edu/wordpress/wp-content/uploads/2015/04/dvs_031.pdf), [YouTube](https://youtu.be/m7qOEsTyVwU), [Project page](http://compphotolab.northwestern.edu/project/mc3d-motion-contrast-3d-laser-scanner/)

<a name="depth-stereo"></a>
### Stereo Depth Estimation
- Rogister, P. , Benosman, R., Ieng, S.-H., Lichtsteiner, P., Delbruck, T., [Asynchronous Event-Based Binocular Stereo Matching](https://doi.org/10.1109/TNNLS.2011.2180025), IEEE Trans. Neural Networks and Learning Systems, 23(2):347--353, 2012.
- Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Ieng, S. H., Benosman, R. B., and Linares-Barranco, B., [On the use of orientation filters for 3D reconstruction in event–driven stereo vision](https://doi.org/10.3389/fnins.2014.00048). Front. Neurosci. (2014) 8:48.
- Camuñas-Mesa, L. A., Serrano-Gotarredona, T., Linares-Barranco, B., Ieng, S., Benosman, R., [Event-Driven Stereo Vision with Orientation Filters](https://doi.org/10.1109/ISCAS.2014.6865114), IEEE Int. Symp. Circuits and Systems (ISCAS), Melbourne VIC, 2014, pp. 257--260.


<a name="optical-flow"></a>
## Optical Flow Estimation
- *[Cook et. al. IJCNN 2011](#Cook11ijcnn)*; in case of rotational motion.
- Benosman, R., Ieng, S.-H., Clercq, C., Bartolozzi, C., and Srinivasan, M., *[Asynchronous Frameless Event-Based Optical Flow](https://doi.org/10.1016/j.neunet.2011.11.001)*. Neural Networks (2012), 27:32-37.
- Benosman, R., Clercq, C., Lagorce, X., Ieng, S.-H., and Bartolozzi, C., *[Event-Based Visual Flow](https://doi.org/10.1109/TNNLS.2013.2273537)*. IEEE Trans. Neural Networks and Learning Systems (2014), 25(2):407--417.
- E. Mueggler, C. Forster, N. Baumli, G. Gallego, D. Scaramuzza, *[Lifetime Estimation of Events from Dynamic Vision Sensors](http://dx.doi.org/10.1109/ICRA.2015.7139876)*, IEEE Int. Conf. Robotics and Automation (ICRA), Seattle (WA), USA, 2015, pp. 4874--4881. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA15_Mueggler.pdf), [Code](https://www.github.com/uzh-rpg/rpg_event_lifetime)
- Tschechne, S., Sailer R., Neumann, H., *[Bio-Inspired Optic Flow from Event-Based Neuromorphic Sensor Input](https://doi.org/10.1007/978-3-319-11656-3_16)*, IAPR Workshop on Artificial Neural Networks in Pattern Recognition (ANNPR) 2014, pp. 171-182.
- J. Conradt, *[On-Board Real-Time Optic-Flow for Miniature Event-Based Vision Sensors](https://doi.org/10.1109/ROBIO.2015.7419043)*, 2015 IEEE International Conference on Robotics and Biomimetics (ROBIO), Zhuhai, 2015, pp. 1858-1863.
- Brosch, T., Tschechne, S., Neumann, H., *[On event-based optical flow detection](https://doi.org/10.3389/fnins.2015.00137)*, Front. Neurosci. (2015), 9:137.
- Kosiorek, A., Adrian, D., Rausch, J., Conradt, J., *[An Efficient Event-Based Optical Flow Implementation in C/C++ and CUDA](https://www.nst.ei.tum.de/fileadmin/w00bqs/www/publications/pp/2015SS-PP-RealTimeDVSOpticFlow.pdf)*. Tech. Rep. TU Munich, 2015.
- Rueckauer, B. and Delbruck, T., *[Evaluation of Event-Based Algorithms for Optical Flow with Ground-Truth from Inertial Measurement Sensor](https://doi.org/10.3389/fnins.2016.00176)*. Front. Neurosci (2016). 10:176.
- <a name="Bardow16cvpr"></a>Bardow, P. A., Davison, A. J., Leutenegger, S., *[Simultaneous Optical Flow and Intensity Estimation](http://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Bardow_Simultaneous_Optical_Flow_CVPR_2016_paper.pdf)*, Computer Vision and Pattern Recognition (CVPR), Las Vegas, USA, 2016. [YouTube](https://youtu.be/1zqJpiheaaI)
- Liu, M., Delbruck, T., *[Block-Matching Optical Flow for Dynamic Vision Sensors: Algorithm and FPGA Implementation](https://arxiv.org/pdf/1706.05415.pdf)*, IEEE Int. Symp. Circuits and Systems (ISCAS), Baltimore, MD, 2017.


<a name="image-reconstruction"></a>
## Intensity-Image Reconstruction from events
- <a name="Cook11ijcnn"></a>Cook, M., Gugelmann, L., Jug, F., Krautz, C., Steger, A., *[Interacting maps for fast visual interpretation](https://doi.org/10.1109/IJCNN.2011.6033299)*, Int. Joint Conf. on Neural Networks (IJCNN), San Jose, CA, 2011, pp. 770--776. [YouTube](https://youtu.be/irX3Nd5U0hY)
- Kim, H., Handa, A., Benosman, R., Ieng, S.-H., Davison, A.J., *[Simultaneous Mosaicing and Tracking with an Event Camera](http://www.bmva.org/bmvc/2014/papers/paper066/)*, British Machine Vision Conference, 2014. [PDF](http://www.bmva.org/bmvc/2014/files/paper066.pdf), [YouTube](https://youtu.be/l6qxeM1DbXU).
    - [Code for intensity reconstruction](https://github.com/uzh-rpg/rpg_image_reconstruction_from_events).
- *[Bardow et. al. CVPR 2016](#Bardow16cvpr)*
- Reinbacher, C., Graber, G., Pock, T., *[Real-Time Intensity-Image Reconstruction for Event Cameras Using Manifold Regularisation](http://www.bmva.org/bmvc/2016/papers/paper009/)*, British Machine Vision Conference (BMVC), York, 2016. [PDF](http://www.bmva.org/bmvc/2016/papers/paper009/paper009.pdf), [YouTube](https://youtu.be/rvB2URrGT94), [Code](https://github.com/VLOGroup/dvs-reconstruction)


<a name="egomotion"></a>
## Localization and Ego-Motion Estimation
- *[Cook et. al. IJCNN 2011](#Cook11ijcnn)*; in case of rotational motion.
- Weikersdorfer, D. and Conradt, J., *[Event-based particle filtering for robot self-localization](http://doi.org/10.1109/ROBIO.2012.6491077)*, IEEE Int. Conf. on Robotics and Biomimetcs (ROBIO), Guangzhou, 2012, pp. 866--870. [PDF](https://mediatum.ub.tum.de/doc/1215541/835468.pdf)
- Censi, A., Strubel, J., Brandli, C., Delbruck, T., Scaramuzza, D., *[Low-latency localization by Active LED Markers tracking using a Dynamic Vision Sensor](https://doi.org/10.1109/IROS.2013.6696456)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Tokyo, 2013. [PDF](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.pdf) [PPT](http://rpg.ifi.uzh.ch/docs/IROS13_Censi.ppt)
- Mueggler, E., Huber, B., Scaramuzza, D., *[Event-based, 6-DOF Pose Tracking for High-Speed Maneuvers](https://doi.org/10.1109/IROS.2014.6942940)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Chicago, IL, 2014, pp. 2761--2768. [PDF](http://rpg.ifi.uzh.ch/docs/IROS14_Mueggler.pdf), [YouTube](https://youtu.be/LauQ6LWTkxM)
- Gallego, G., Forster, C., Mueggler, E., Scaramuzza, D., *[Event-based Camera Pose Tracking using a Generative Event Model](https://arxiv.org/pdf/1510.01972v1)*, arXiv:1510.01972, 2015.
- Mueggler, E., Gallego G., Scaramuzza, D., *[Continuous-Time Trajectory Estimation for Event-based Vision Sensors](http://dx.doi.org/10.15607/RSS.2015.XI.036)*. Robotics: Science and Systems XI (RSS), Rome, Italy, 2015. [PDF]
- Gallego, G., Lund, J.E.A., Mueggler, E., Rebecq, H., Delbruck, T., Scaramuzza, D., *[Event-based, 6-DOF Camera Tracking for High-Speed Applications](https://arxiv.org/pdf/1607.03468.pdf)*, (Under review), 2016. [YouTube](https://youtu.be/iZZ77F-hwzs)
- Reinbacher, C., Munda, G., Pock, T., *[Real-Time Panoramic Tracking for Event Cameras](https://doi.org/10.1109/ICCPHOT.2017.7951488)*, IEEE Int. Conf. Computational Photography (ICCP), Stanford, CA, USA, 2017, pp. 1--9. [PDF](https://arxiv.org/abs/1703.05161), [YouTube](https://youtu.be/Qy0brSlirmk), [Code](https://github.com/VLOGroup/dvs-panotracking)


<a name="VOSLAM"></a>
## Visual Odometry and SLAM (Simultaneous Localization And Mapping)
- Weikersdorfer, D., Hoffmann, R., Conradt. J., *[Simultaneous localization and mapping for event-based vision systems](http://doi.org/10.1007/978-3-642-39402-7_14)*. Int. Conf. Computer Vision Systems (ICVS), 2013, pp. 133--142. [PDF](https://mediatum.ub.tum.de/doc/1191908/271955.pdf), [Slides](http://workshops.acin.tuwien.ac.at/ICVS/downloads/ICVS2013-ebslam_weikersdorfer.pdf)
- Censi, A. and Scaramuzza, D., *[Low-latency Event-based Visual Odometry](https://doi.org/10.1109/ICRA.2014.6906931)*, IEEE Int. Conf. Robotics and Automation (ICRA), Hong-Kong, 2014, pp. 703--710. [PDF](http://rpg.ifi.uzh.ch/docs/ICRA14_Censi.pdf), [Slides](https://censi.science/pub/research/2013-dvsd/201405-icra15-dvsd.pdf)
- Weikersdorfer, D., Adrian, D. B., Cremers, D., Conradt, J., *[Event-based 3D SLAM with a depth-augmented dynamic vision sensor](https://doi.org/10.1109/ICRA.2014.6906882)*, IEEE Int. Conf. Robotics and Automation (ICRA), Hong-Kong, 2014, pp. 359--364.
- Kueng, B., Mueggler, E., Gallego, G., Scaramuzza, D., *[Low-Latency Visual Odometry using Event-based Feature Tracks](https://doi.org/10.1109/IROS.2016.7758089)*, IEEE/RSJ Int. Conf. Intelligent Robots and Systems (IROS), Daejeon, South Korea, 2016, pp. 16--23. [PDF](http://rpg.ifi.uzh.ch/docs/IROS16_Kueng.pdf). [YouTube](https://youtu.be/RDu5eldW8i8)
- Kim, H., Leutenegger, S., Davison, A.J., *[Real-Time 3D Reconstruction and 6-DoF Tracking with an Event Camera](http://doi.org/10.1007/978-3-319-46466-4_21)*, European Conference on Computer Vision (ECCV), 2016, pp. 349--364. [PDF](https://www.doc.ic.ac.uk/~ajd/Publications/kim_etal_eccv2016.pdf), [YouTube](https://youtu.be/yHLyhdMSw7w)
- Rebecq, H., Horstschaefer, T., Gallego, G., Scaramuzza, D., *[EVO: A Geometric Approach to Event-based 6-DOF Parallel Tracking and Mapping in Real-time](https://doi.org/10.1109/LRA.2016.2645143)*, IEEE Robotics and Automation Letters (RA-L), 2:2(593--600), 2017. [PDF](http://rpg.ifi.uzh.ch/docs/RAL16_EVO.pdf), [Youtube](https://youtu.be/bYqD2qZJlxE).
- Gallego, G. and Scaramuzza, D., *[Accurate Angular Velocity Estimation with an Event Camera](https://doi.org/10.1109/LRA.2016.2647639)*. IEEE Robotics and Automation Letters (RA-L), 2:2(632--639), 2017.
[PDF](http://rpg.ifi.uzh.ch/docs/RAL16_Gallego.pdf), [Youtube](https://youtu.be/v1sXWoOAs_0).


<a name="visual-inertial"></a>
## Visual-Inertial State Estimation
- Mueggler, E., Gallego, G., Rebecq, H., Scaramuzza, D., *[Continuous-Time Visual-Inertial Trajectory Estimation with Event Cameras](https://arxiv.org/pdf/1702.07389.pdf)*, (Under review), 2017.
- Zhu, A., Atanasov, N., Daniilidis, K., Event-based Visual Inertial Odometry, Conf. Computer Vision and Pattern Recognition (CVPR) 2017.


<a name="camera-stabilization"></a>
## Camera Stabilization
- Delbruck, T., Villanueva, V., and Longinotti, L., *[Integration of dynamic vision sensor with inertial measurement unit for electronically stabilized event-based vision](http://doi.org/10.1109/ISCAS.2014.6865714)*, IEEE Int. Symp. Circuits and Systems (ISCAS) 2014, 2636--2639.


<a name="datasets"></a>
## Datasets
- [Several datasets from the Sensors group at INI](http://sensors.ini.uzh.ch/databases.html) (Institute of Neuroinformatics), Zurich:
    - DDD17 - DAVIS Driving Dataset 2017
    - Predator/Prey Dataset
    - [DVS Datasets for Object Tracking, Action Recognition and Object Recognition](http://dgyblog.com/projects-term/dvs-dataset.html)
    - DVS/DAVIS Optical Flow Dataset
    - [DVS128 Dynamic Vision Sensor Silicon Retina data](https://sourceforge.net/p/jaer/wiki/AER%20data/)
- [Combined Dynamic Vision / RGB-D Dataset](http://ci.nst.ei.tum.de/EBSLAM3D/dataset/), from the paper Weikersdorfer, D., Adrian, D. B., Cremers, D., Conradt, J., *[Event-based 3D SLAM with a depth-augmented dynamic vision sensor](https://doi.org/10.1109/ICRA.2014.6906882)*, Int. Conf. Robotics and Automation (ICRA), Hong-Kong, pp. 359--364, 2014.
- Rueckauer, B. and Delbruck, T., [Evaluation of Event-Based Algorithms for Optical Flow with Ground-Truth from Inertial Measurement Sensor](https://doi.org/10.3389/fnins.2016.00176). Front. Neurosci (2016). 10:176.
- Barranco, F., Fermuller, C., Aloimonos, Y., [A Dataset for Visual Navigation with Neuromorphic Methods](https://dx.doi.org/10.3389%2Ffnins.2016.00049). Front. Neurosci. 10:49.
- E. Mueggler, H. Rebecq, G. Gallego, T. Delbruck, D. Scaramuzza, [The Event-Camera Dataset and Simulator: Event-based Data for Pose Estimation, Visual Odometry, and SLAM](http://rpg.ifi.uzh.ch/davis_data.html), Int. J. Robotics Research, 36:2, pp. 142--149, 2017. [PDF](https://arxiv.org/pdf/1610.08336.pdf), [PDF IJRR](http://dx.doi.org/10.1177/0278364917691115), [Dataset](http://rpg.ifi.uzh.ch/davis_data.html).
- Hu, Y., Liu, H., Pfeiffer, M., Delbruck, T., [DVS Benchmark Datasets for Object Tracking, Action Recognition, and Object Recognition](https://doi.org/10.3389/fnins.2016.00405). Front. Neurosci. 10:405.
- Binas, J., Neil, D., Liu, S.-C., Delbruck, T., *[DDD17: End-To-End DAVIS Driving Dataset](https://www.openreview.net/pdf?id=HkehpKVG-)*. In Proc. 34th Int. Conf. Machine Learning, Sydney, Australia, PMLR 70,  2017. [Dataset](http://sensors.ini.uzh.ch/databases.html)


## Recognition
- Lee, J., Delbruck, T., Park, P. K. J., Pfeiffer, M., Shin, C. W., Ryu, H., Kang, B. C., [Live demonstration: Gesture-Based remote control using stereo pair of dynamic vision sensors](https://doi.org/10.1109/ISCAS.2012.6272144). IEEE Int. Symp. Circuits and Systems (ISCAS) 2012, Seoul, South Korea, pp. 736--740. [PDF](http://www.zora.uzh.ch/75315/1/Lee_et_al_Live_demonstration.pdf), [YouTube]()


### Neural Networks
- <a name="MoeysEBCCSP16"></a>Moeys, D., Corradi F., Kerr, E., Vance, P., Das, G., Neil, D., Kerr, D., Delbruck, T., [Steering a Predator Robot using a Mixed Frame/Event-Driven Convolutional Neural Network](https://doi.org/10.1109/EBCCSP.2016.7605233), IEEE Int. Conf. Event-Based Control Comm. and Signal Proc. (EBCCSP), Krakow, Poland, 2016. [PDF]


## Control
- Conradt, J., Cook, M., Berner, R., Lichtsteiner, P., Douglas, R. J., Delbruck, T., [A Pencil Balancing Robot Using a Pair of AER Dynamic Vision Sensors](https://doi.org/10.1109/ISCAS.2009.5117867), IEEE Int. Symp. Circuits and Systems (ISCAS) 2009, pp. 781--784, 2009.
<!-- - Conradt, J., Berner, R., Cook, M., Delbruck, T., [An embedded AER dynamic vision sensor for low-latency pole balancing](https://doi.org/10.1109/ICCVW.2009.5457625), IEEE Int. Conf. Computer Vision Workshops (ICCVW), Kyoto, Japan, 2009. [PDF](www.ini.uzh.ch/admin/extras/doc_get.php?id=42580) -->
- Delbruck, T., Lang, M., [Robotic Goalie with 3ms Reaction Time at 4% CPU Load Using Event-Based Dynamic Vision Sensor](https://doi.org/10.3389/fnins.2013.00223), Front. Neurosci. (2013) 7:223. [PDF](http://www.zora.uzh.ch/107801/1/fnins-07-00223.pdf), [YouTube](https://youtu.be/IC5x7ftJ96w)
- Censi, A., [Efficient Neuromorphic Optomotor Heading Regulation](https://doi.org/10.1109/ACC.2015.7171931), The 2015 American Control Conference (ACC), Chicago, IL, 2015, pp. 3854--3861.
- [Moeys et. al. EBCCSP 2016](#MoeysEBCCSP16)


## Neuromorphic Processors and Platforms
- [Dynamic Neuromorphic Asynchronous Processor (DYNAP) by iniLabs](https://inilabs.com/products/dynap/)
  - Qiao, N., Mostafa, H., Corradi, F., Osswald, M., Stefanini, F., Sumislawska, D., Indiveri, G. [A reconfigurable on-line learning spiking neuromorphic processor comprising 256 neurons and 128K synapses](https://doi.org/10.3389/fnins.2015.00141). Front. Neurosci. (2015) 9:141. [PDF](https://capocaccia.ethz.ch/capo/raw-attachment/wiki/2015/hybrid15/frontiers14-nlp.pdf)
  - Indiveri, G., Qiao, N., Corradi, F., [Neuromorphic Architectures for Spiking Deep Neural Networks](https://doi.org/10.1109/IEDM.2015.7409623), IEEE Int. Electron Devices Meeting (IEDM), Washington, DC, 2015, pp. 4.2.1--4.2.4. [PDF](http://ncs.ethz.ch/pubs/pdf/Indiveri_etal15.pdf)
- Galluppi, F., Denk, C., Meiner, M. C., Stewart, T. C., Plana, L. A., Eliasmith, C., Furber, S., Conradt, J., [Event-based neural computing on an autonomous mobile platform](https://doi.org/10.1109/ICRA.2014.6907270), IEEE Int. Conf. Robotics and Automation (ICRA), Hong Kong, 2014, pp. 2862--2867. [PDF](http://compneuro.uwaterloo.ca/files/publications/galluppi.2014.pdf)


<a name="workshops"></a>
## Workshops
- [ICRA 2015 Workshop on Innovative Sensing for Robotics](http://innovative-sensing.mit.edu/), with a focus on Neuromorphic Sensors.
- [ICRA 2017 First International Workshop on Event-based Vision](http://rpg.ifi.uzh.ch/ICRA17_event_vision_workshop.html).
- [The Telluride Neuromorphic Cognition Engineering Workshops](http://telluride.iniforum.ch/accounts/login/?next=/).
- [Capo Caccia Workshops toward Cognitive Neuromorphic Engineering](http://capocaccia.iniforum.ch/).


## People / Research Groups
- [Institute of NeuroInformatics](https://www.ini.uzh.ch/) (INI)  of the University of Zurich (UZH) and ETH Zurich.
- [iniLabs](http://www.inilabs.com) (Comerzialization of neuromorphic technology from INI).
- [Robotics and Perception Group](http://rpg.ifi.uzh.ch/research_dvs.html) (RPG-UZH).
