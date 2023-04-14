# Inference System

System for machine learning inference.

## Benchmark
- Wanling Gao, Fei Tang, Jianfeng Zhan, et al. "AIBench: A Datacenter AI Benchmark Suite, BenchCouncil". [[Paper]](https://arxiv.org/pdf/2005.03459.pdf) [[Website]](https://www.benchcouncil.org/AIBench/index.html)
- BaiduBench: Benchmarking Deep Learning operations on different hardware. [[Github]](https://github.com/baidu-research/DeepBench#inference-benchmark)
- Reddi, Vijay Janapa, et al. "Mlperf inference benchmark." arXiv preprint arXiv:1911.02549 (2019). [[Paper]](https://arxiv.org/pdf/1911.02549.pdf) [[GitHub]](https://github.com/mlperf/inference)
- Bianco, Simone, et al. "Benchmark analysis of representative deep neural network architectures." IEEE Access 6 (2018): 64270-64277. [[Paper]](https://arxiv.org/abs/1810.00736)
- Almeida, Mario, et al. "EmBench: Quantifying Performance Variations of Deep Neural Networks across Modern Commodity Devices." The 3rd International Workshop on Deep Learning for Mobile Systems and Applications. 2019. [[Paper]](https://arxiv.org/pdf/1905.07346.pdf)

## Model Management

- Model Card Toolkit. The Model Card Toolkit (MCT) streamlines and automates generation of Model Cards [1], machine learning documents that provide context and transparency into a model's development and performance. [[Paper]](https://arxiv.org/pdf/1810.03993.pdf) [[GitHub]](https://github.com/tensorflow/model-card-toolkit)
- DLHub: Model and data serving for science.  [[Paper]](https://arxiv.org/pdf/1811.11213.pdf)
  - Chard, R., Li, Z., Chard, K., Ward, L., Babuji, Y., Woodard, A., Tuecke, S., Blaiszik, B., Franklin, M. and Foster, I., 2019, May. 
  - In 2019 IEEE International Parallel and Distributed Processing Symposium (IPDPS) (pp. 283-292). IEEE. 
- Publishing and Serving Machine Learning Models with DLHub. [[Paper]](https://dl.acm.org/doi/10.1145/3332186.3332246)
- TRAINS - Auto-Magical Experiment Manager & Version Control for AI [[GitHub]](https://github.com/allegroai/trains)
- ModelDB: A system to manage ML models [[GitHub]](https://github.com/mitdbg/modeldb) [[MIT short paper]](https://mitdbg.github.io/modeldb/papers/hilda_modeldb.pdf)
- iterative/dvc: Data & models versioning for ML projects, make them shareable and reproducible [[GitHub]](https://github.com/iterative/dvc)

## Model Serving

- Announcing RedisAI 1.0: AI Serving Engine for Real-Time Applications [[Blog]](https://redislabs.com/blog/redisai-ai-serving-engine-for-real-time-applications/)
- $\color{red}{(Read)(New)}$ Serving Heterogeneous Machine Learning Models on Multi-GPU Servers with Spatio-Temporal Sharing (ATC'22) [[paper]](https://www.usenix.org/system/files/atc22-choi-seungbeom.pdf)[[code]](https://github.com/casys-kaist/glet)
  - Seungbeom Choi, Sunho Lee, Yeonjae Kim, Jongse Park, Youngjin Kwon and Jaehyuk Huh (Korea Advanced Institute of Science and Technology, KAIST)
  - ATC'22
  - Summary (2023/4/14 by Liang): 
- $\color{red}{(Read)(New)}$ Trueno: A Cross-Platform Machine Learning Model Serving Framework in Heterogeneous Edge Systems
  - Danyang Song∗, Yifei Zhu†(SJTU), Cong Zhang‡, and Jiangchuan Liu
  - INFOCOM'22 DEMO
- $\color{red}{(Read)(New)}$ SHEPHERD: Serving DNNs in the Wild [[paper]](https://hongzhangblaze.github.io/assets/pdf/shepherd.pdf)
  - Hong Zhang (University of Waterloo), Yupeng Tang, Anurag Khandelwal (Yale University), Ion Stoica (UC Berkeley)
  - NSDI 2023
- $\color{red}{(New)}$ ORLOJ: Predictably Serving Unpredictable DNNs [[paper]](https://arxiv.org/pdf/2209.00159.pdf)
  - Peifeng Yu, Yuqing Qiu, Xin Jin, Mosharaf Chowdhury (University of Michigan)
  - arXiv
  - Summary: A distribution-aware dynamic
DNN serving system, to provide high throughput and
low SLO misses. ORLOJ also takes a plan-ahead approach, but
unlike recent solutions, it uses a random variable to capture
the variance in request execution times of dynamic DNNs,
rather than assuming a constant mean or tail latency for all
requests. This gives ORLOJ more flexibility to account for
uncertainty in execution times when batching them together
to achieve high throughput. [[detailed notes]](zl_notes/ORLOJ.md#ORLOJ)
- Cloudburst: Stateful Functions-as-a-Service. [\[Paper\]](https://arxiv.org/pdf/2001.04592.pdf) [\[GitHub\]](https://github.com/hydro-project/cloudburst)
  - Vikram Sreekanti, Chenggang Wu, Xiayue Charles Lin, Johann Schleier-Smith, Joseph E. Gonzalez, Joseph M. Hellerstein, Alexey Tumanov
  - VLDB 2020
  - A stateful FaaS platform.
    (1) feasibility of general-purpose stateful serverless computing. 
    (2) Autoscaling via logical disaggregation of storage and compute, state management via physical 
    colocation of caches with compute services.
    (3) LDPC design pattern
- Optimizing Prediction Serving on Low-Latency Serverless Dataflow [[Paper]](https://arxiv.org/pdf/2007.05832.pdf)
  - Sreekanti, Vikram, Harikaran Subbaraj, Chenggang Wu, Joseph E. Gonzalez, and Joseph M. Hellerstein.
  - arXiv preprint arXiv:2007.05832 (2020).
- $\color{red}{(Read)}$ Serving DNNs like Clockwork: Performance Predictability from the Bottom Up. [[Paper]](https://arxiv.org/pdf/2006.02464.pdf)
  - Gujarati, A., Karimi, R., Alzayat, S., Kaufmann, A., Vigfusson, Y. and Mace, J., 2020.
  - OSDI 2020
  - Summary (2023.4.12 by Liang): A istributed model serving system with predictable performance based on consolidating choice approach (eschewing reactive and best-effort mechanisms
and centralizing all resource consumption and scheduling
decisions) to mitigates tail latency and achieves ideal goodput [[detailed notes]](zl_notes/Clockwork.md#clockwork)
- Swayam: distributed autoscaling to meet SLAs of machine learning inference services with resource efficiency [[Paper]](https://www.microsoft.com/en-us/research/uploads/prod/2018/01/2017.Middleware.Swayam.TailLatencyInAzureML.pdf)[[Code]](https://gitlab.mpi-sws.org/cld/ml/clockwork)
  - Gujarati, Arpan, Sameh Elnikety, Yuxiong He, Kathryn S. McKinley, and Björn B. Brandenburg.
  - In Proceedings of the 18th ACM/IFIP/USENIX Middleware Conference, pp. 109-120. 2017.
  - Summary: a cloud autoscaler. (1) model-based autoscaling that takes into account SLAs and ML inference workload characteristics, (2) a distributed protocol that uses partial load information and prediction at frontends to provi- sion new service instances, and (3) a backend self-decommissioning protocol for service instances
- Swift machine learning model serving scheduling: a region based reinforcement learning approach. [[Paper]](https://dl.acm.org/doi/10.1145/3295500.3356164) [[GitHub]](https://github.com/SC-RRL/RRL)
  - Qin, Heyang, Syed Zawad, Yanqi Zhou, Lei Yang, Dongfang Zhao, and Feng Yan.
  - In Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis, pp. 1-23. 2019.
  - Summary: The system performances under different similar con- figurations in a region can be accurately estimated by using the system performance under one of these configurations, due to their similarity. Region based DRL is designed for parallelism selection.
- TorchServe is a flexible and easy to use tool for serving PyTorch models. [[GitHub]](https://github.com/pytorch/serve)
- Seldon Core: Blazing Fast, Industry-Ready ML. An open source platform to deploy your machine learning models on Kubernetes at massive scale. [[GitHub]](https://github.com/SeldonIO/seldon-core)
- MArk: Exploiting Cloud Services for Cost-Effective, SLO-Aware Machine Learning Inference Serving [[Paper]](https://www.usenix.org/system/files/atc19-zhang-chengliang.pdf) [[GitHub]](https://github.com/marcoszh/MArk-Project)
  - Zhang, C., Yu, M., Wang, W. and Yan, F., 2019. 
  - In 2019 {USENIX} Annual Technical Conference ({USENIX}{ATC} 19) (pp. 1049-1062).
  - Summary: address the scalability and cost minimization issues for model serving on the public cloud.
- Parity Models: Erasure-Coded Resilience for Prediction Serving Systems(SOSP2019) [[Paper]](http://www.cs.cmu.edu/~rvinayak/papers/sosp2019parity-models.pdf) [[GitHub]](https://github.com/Thesys-lab/parity-models)
- INFaaS: A Model-less Inference Serving System Romero [[Paper]](https://arxiv.org/abs/1905.13348) [[GitHub]](https://github.com/stanford-mast/INFaaS)
  - F., Li, Q., Yadwadkar, N.J. and Kozyrakis, C., 2019.
  - arXiv preprint arXiv:1905.13348.
- Nexus: Nexus is a scalable and efficient serving system for DNN applications on GPU cluster (SOSP2019) [[Paper]](https://pdfs.semanticscholar.org/0c0f/353dbac84311ea4f1485d4a8ac0b0459be8c.pdf) [[GitHub]](https://github.com/uwsampl/nexus)
- Deep Learning Inference Service at Microsoft [[Paper]](https://www.usenix.org/system/files/opml19papers-soifer.pdf)
  - J Soifer, et al. (*OptML2019*)
- {PRETZEL}: Opening the Black Box of Machine Learning Prediction Serving Systems. [[Paper]](https://www.usenix.org/system/files/osdi18-lee.pdf)
  - Lee, Y., Scolari, A., Chun, B.G., Santambrogio, M.D., Weimer, M. and Interlandi, M., 2018. (*OSDI 2018*)
- Brusta: PyTorch model serving project [[GitHub]](https://github.com/hyoungseok/brusta)
- Model Server for Apache MXNet: Model Server for Apache MXNet is a tool for serving neural net models for inference [[GitHub]](https://github.com/awslabs/mxnet-model-server)
- TFX: A TensorFlow-Based Production-Scale Machine Learning Platform [[Paper]](http://stevenwhang.com/tfx_paper.pdf) [[Website]](https://www.tensorflow.org/tfx) [[GitHub]](https://github.com/tensorflow/tfx)
  - Baylor, Denis, et al. (*KDD 2017*)
- Tensorflow-serving: Flexible, high-performance ml serving [[Paper]](https://arxiv.org/pdf/1712.06139) [[GitHub]](https://github.com/tensorflow/serving)
  - Olston, Christopher, et al.
- IntelAI/OpenVINO-model-server: Inference model server implementation with gRPC interface, compatible with TensorFlow serving API and OpenVINO™ as the execution backend. [[GitHub]](https://github.com/IntelAI/OpenVINO-model-server)
- Clipper: A Low-Latency Online Prediction Serving System [[Paper]](https://www.usenix.org/system/files/conference/nsdi17/nsdi17-crankshaw.pdf)
[[GitHub]](https://github.com/ucbrise/clipper)
  - Crankshaw, Daniel, et al. (*NSDI 2017*)
  - Summary: Adaptive batch 
- InferLine: ML Inference Pipeline Composition Framework [[Paper]](https://arxiv.org/pdf/1812.01776.pdf) [[GitHub]](https://github.com/simon-mo/inferline-models)
  - Crankshaw, Daniel, et al. (*SoCC 2020*)
  - Summary: update version of Clipper
- TrIMS: Transparent and Isolated Model Sharing for Low Latency Deep LearningInference in Function as a Service Environments [[Paper]](https://arxiv.org/pdf/1811.09732.pdf)
  - Dakkak, Abdul, et al (*Preprint*)
  - Summary: model cold start problem
- Rafiki: machine learning as an analytics service system [[Paper]](http://www.vldb.org/pvldb/vol12/p128-wang.pdf) [[GitHub]](https://github.com/nginyc/rafiki)
  - Wang, Wei, Jinyang Gao, Meihui Zhang, Sheng Wang, Gang Chen, Teck Khim Ng, Beng Chin Ooi, Jie Shao, and Moaz Reyad.
  - Summary: Contain both training and inference. Auto-Hype-Parameter search for training. Ensemble models for inference. Using DRL to balance trade-off between accuracy and latency.
- GraphPipe: Machine Learning Model Deployment Made Simple [[GitHub]](https://github.com/oracle/graphpipe)
- Orkhon: ML Inference Framework and Server Runtime [[GitHub]](https://github.com/vertexclique/orkhon)
- NVIDIA/tensorrt-inference-server: The TensorRT Inference Server provides a cloud inferencing solution optimized for NVIDIA GPUs. [[GitHub]](https://github.com/NVIDIA/tensorrt-inference-server) [[Slides: DEEP INTO TRTIS]](https://on-demand.gputechconf.com/gtc-cn/2019/pdf/CN9506/presentation.pdf) 
- INFaaS: Automated Model-less Inference Serving [[GitHub]](https://github.com/stanford-mast/INFaaS), [[Paper]](https://www.usenix.org/conference/atc21/presentation/romero)
  - Francisco Romero, Qian Li, Neeraja J. Yadwadkar, and Christos Kozyrakis (*ATC 2021*)
- Llama: A Heterogeneous & Serverless Framework for Auto-Tuning Video Analytics Pipelines
  - Francisco Romero, Mark Zhao, Neeraja J. Yadwadkar, and Christos Kozyrakis (*SoCC 2021*)
- Scrooge: A Cost-Effective Deep Learning Inference System [[Paper]](https://dl.acm.org/doi/pdf/10.1145/3472883.3486993)
  - Yitao Hu, Rajrup Ghosh, Ramesh Govindan
- Apache PredictionIO® is an open source Machine Learning Server built on top of a state-of-the-art open source stack for developers and data scientists to create predictive engines for any machine learning task [[Website]](http://predictionio.apache.org/)

## Cache for Inference

- Kumar, Adarsh, et al. "Accelerating deep learning inference via freezing." 11th {USENIX} Workshop on Hot Topics in Cloud Computing (HotCloud 19). 2019. [[Paper]](http://shivaram.org/publications/freeze-hotcloud19.pdf)
- Xu, Mengwei, et al. "DeepCache: Principled cache for mobile deep vision." Proceedings of the 24th Annual International Conference on Mobile Computing and Networking. 2018. [[Paper]](https://arxiv.org/pdf/1712.01670.pdf)
- Park, Keunyoung, and Doo-Hyun Kim. "Accelerating image classification using feature map similarity in convolutional neural networks." Applied Sciences 9.1 (2019): 108. [[Paper]](https://www.mdpi.com/2076-3417/9/1/108/htm)
- Cavigelli, Lukas, and Luca Benini. "CBinfer: Exploiting frame-to-frame locality for faster convolutional network inference on video streams." IEEE Transactions on Circuits and Systems for Video Technology (2019). [[Paper]](https://arxiv.org/pdf/1808.05488)

## Inference Optimization

- Jointly Optimizing Preprocessing and Inference for DNN-based Visual Analytics [[Paper]](https://arxiv.org/pdf/2007.13005.pdf)
  - Daniel Kang, Ankit Mathur, Teja Veeramacheneni, Peter Bailis, Matei Zaharia
  - VLDB 2021 
- Willump: A Statistically-Aware End-to-end Optimizer for Machine Learning Inference. [[arxiv]](https://arxiv.org/pdf/1906.01974.pdf)[[GitHub]](https://github.com/stanford-futuredata/Willump)
  - Peter Kraft, Daniel Kang, Deepak Narayanan, Shoumik Palkar, Peter Bailis, Matei Zaharia.
  - arXiv Preprint. 2019.
- TensorRT is a C++ library that facilitates high performance inference on NVIDIA GPUs and deep learning accelerators. [[GitHub]](https://github.com/NVIDIA/TensorRT)
- Dynamic Space-Time Scheduling for GPU Inference [[Paper]](http://learningsys.org/nips18/assets/papers/102CameraReadySubmissionGPU_Virtualization%20(8).pdf) [[GitHub]](https://github.com/ucbrise/caravel)
  - Jain, Paras, et al. (*NIPS 18, System for ML*)
  - Summary: optimization for GPU Multi-tenancy
- Dynamic Scheduling For Dynamic Control Flow in Deep Learning Systems [[Paper]](http://www.cs.cmu.edu/~jinlianw/papers/dynamic_scheduling_nips18_sysml.pdf)
  - Wei, Jinliang, Garth Gibson, Vijay Vasudevan, and Eric Xing. (*On going*)
- Accelerating Deep Learning Workloads through Efficient Multi-Model Execution. [[Paper]](https://cs.stanford.edu/~matei/papers/2018/mlsys_hivemind.pdf)
  - D. Narayanan, K. Santhanam, A. Phanishayee and M. Zaharia. (*NeurIPS Systems for ML Workshop 2018*)
  - Summary: They assume that their system, HiveMind, is given as input models grouped into model batches that are amenable to co-optimization and co-execution. a compiler, and a runtime.
- DeepCPU: Serving RNN-based Deep Learning Models 10x Faster [[Paper]](https://www.usenix.org/system/files/conference/atc18/atc18-zhang-minjia.pdf)
  - Minjia Zhang, Samyam Rajbhandari, Wenhan Wang, and Yuxiong He, Microsoft AI and Research (*ATC 2018*)

## Cluster Management for Inference (now only contain multi-tenant)

- Ease. ml: Towards multi-tenant resource sharing for machine learning workloads [[Paper]](http://www.vldb.org/pvldb/vol11/p607-li.pdf) [[GitHub]](https://github.com/DS3Lab/easeml) [[Demo]](http://www.vldb.org/pvldb/vol11/p2054-karlas.pdf)
  - Li, Tian, et al
  - Proceedings of the VLDB Endowment 11.5 (2018): 607-620.
- Perseus: Characterizing Performance and Cost of Multi-Tenant Serving for CNN Models [[Paper]](https://arxiv.org/pdf/1912.02322.pdf)
  - LeMay, Matthew, Shijian Li, and Tian Guo. 
  - arXiv preprint arXiv:1912.02322 (2019).
  
## Machine Learning Compiler
- Hummingbird: Hummingbird is a library for compiling trained traditional ML models into tensor computations. Hummingbird allows users to seamlessly leverage neural network frameworks (such as PyTorch) to accelerate traditional ML models.[[GitHub]](https://github.com/microsoft/hummingbird)
- {TVM}: An Automated End-to-End Optimizing Compiler for Deep Learning [[Paper]](https://www.usenix.org/system/files/osdi18-chen.pdf) [[YouTube]](https://www.youtube.com/watch?v=I1APhlSjVjs) [[Project Website]](https://tvm.ai/)
  - Chen, Tianqi, et al. (*OSDI 2018*)
  - Summary: Automated optimization is very impressive: cost model (rank objective function) + schedule explorer (parallel simulated annealing)
- Facebook TC: Tensor Comprehensions (TC) is a fully-functional C++ library to automatically synthesize high-performance machine learning kernels using Halide, ISL and NVRTC or LLVM. [[GitHub]](https://github.com/facebookresearch/TensorComprehensions)
- Tensorflow/mlir: "Multi-Level Intermediate Representation" Compiler Infrastructure [[GitHub]](https://github.com/tensorflow/mlir) [[Video]](https://www.youtube.com/watch?v=qzljG6DKgic)
- PyTorch/glow: Compiler for Neural Network hardware accelerators [[GitHub]](https://github.com/pytorch/glow)
- TASO: Optimizing Deep Learning Computation with Automatic Generation of Graph Substitutions [[Paper]](https://cs.stanford.edu/~matei/papers/2019/sosp_taso.pdf) [[GitHub]](https://github.com/jiazhihao/TASO)
  - Jia, Zhihao, Oded Padon, James Thomas, Todd Warszawski, Matei Zaharia, and Alex Aiken. (*SOSP 2019*)
  - Experiments tested on TVM and XLA


## Edge inference
### Memory-efficient
- $\color{red}{(Read)}$ GEMEL: Model Merging for Memory-Efficient, Real-Time Video Analytics at the Edge [[paper]](https://arxiv.org/pdf/2201.07705.pdf)
  - Arthi Padmanabhan, Neil Agarwal, Anand Iyer, Ganesh Ananthanarayanan, Yuanchao Shu, Nikolaos Karianakis, Guoqing Harry Xu, Ravi Netravali (UCLA,Microsoft Research, Princeton University)
  - NSDI'23
  - compare with Nexus
- $\color{red}{(Read)}$ Demand Layering for Real-Time DNN Inference with Minimized Memory Usage [[paper]](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9984745)
  - Mingoo Ji, Saehanseul Yi, Changjin Koo, Sol Ahn, Dongjoo Seo, Nikil Dutt, and Jong-Chan Kim (Kookmin University, Korea)
  - RTSS'22


- YUZU neural-enhanced volumetric video streaming-nsdi22-paper-zhang(NSDI’22,启发式算法)


- Better Together: Jointly Optimizing ML Collective Scheduling and Execution Planning using SYNDICATE 
  - NSDI’23
  - 计算和通信两个维度感知的训练优化

### Energy-efficient
- Balancing energy efficiency and real-time performance in GPU scheduling 
  - RTSS’21
- Towards Energy-Efficient Real-Time Scheduling of Heterogeneous Multi-GPU Systems 
  - RTSS’22

 
