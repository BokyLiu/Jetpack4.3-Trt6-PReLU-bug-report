# ./trtexec output
```
&&&& RUNNING TensorRT.trtexec # ./trtexec --onnx=/home/ubuntu/temp_onnx/face_partial_upload.onnx --saveEngine=/home/ubuntu/temp_onnx/face_partial_upload.trt --fp16 --batch=3 --verbose
[11/20/2019-15:23:10] [I] === Model Options ===
[11/20/2019-15:23:10] [I] Format: ONNX
[11/20/2019-15:23:10] [I] Model: /home/ubuntu/temp_onnx/face_partial_upload.onnx
[11/20/2019-15:23:10] [I] Output:
[11/20/2019-15:23:10] [I] === Build Options ===
[11/20/2019-15:23:10] [I] Max batch: 3
[11/20/2019-15:23:10] [I] Workspace: 16 MB
[11/20/2019-15:23:10] [I] minTiming: 1
[11/20/2019-15:23:10] [I] avgTiming: 8
[11/20/2019-15:23:10] [I] Precision: FP16
[11/20/2019-15:23:10] [I] Calibration: 
[11/20/2019-15:23:10] [I] Safe mode: Disabled
[11/20/2019-15:23:10] [I] Save engine: /home/ubuntu/temp_onnx/face_partial_upload.trt
[11/20/2019-15:23:10] [I] Load engine: 
[11/20/2019-15:23:10] [I] Inputs format: fp32:CHW
[11/20/2019-15:23:10] [I] Outputs format: fp32:CHW
[11/20/2019-15:23:10] [I] Input build shapes: model
[11/20/2019-15:23:10] [I] === System Options ===
[11/20/2019-15:23:10] [I] Device: 0
[11/20/2019-15:23:10] [I] DLACore: 
[11/20/2019-15:23:10] [I] Plugins:
[11/20/2019-15:23:10] [I] === Inference Options ===
[11/20/2019-15:23:10] [I] Batch: 3
[11/20/2019-15:23:10] [I] Iterations: 10 (200 ms warm up)
[11/20/2019-15:23:10] [I] Duration: 10s
[11/20/2019-15:23:10] [I] Sleep time: 0ms
[11/20/2019-15:23:10] [I] Streams: 1
[11/20/2019-15:23:10] [I] Spin-wait: Disabled
[11/20/2019-15:23:10] [I] Multithreading: Enabled
[11/20/2019-15:23:10] [I] CUDA Graph: Disabled
[11/20/2019-15:23:10] [I] Skip inference: Disabled
[11/20/2019-15:23:10] [I] Input inference shapes: model
[11/20/2019-15:23:10] [I] === Reporting Options ===
[11/20/2019-15:23:10] [I] Verbose: Enabled
[11/20/2019-15:23:10] [I] Averages: 10 inferences
[11/20/2019-15:23:10] [I] Percentile: 99
[11/20/2019-15:23:10] [I] Dump output: Disabled
[11/20/2019-15:23:10] [I] Profile: Disabled
[11/20/2019-15:23:10] [I] Export timing to JSON file: 
[11/20/2019-15:23:10] [I] Export profile to JSON file: 
[11/20/2019-15:23:10] [I] 
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - GridAnchor_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - GridAnchorRect_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - NMS_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - Reorg_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - Region_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - Clip_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - LReLU_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - PriorBox_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - Normalize_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - RPROI_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - BatchedNMS_TRT
[11/20/2019-15:23:10] [V] [TRT] Plugin Creator registration succeeded - FlattenConcat_TRT
----------------------------------------------------------------
Input filename:   /home/ubuntu/temp_onnx/face_partial_upload.onnx
ONNX IR version:  0.0.3
Opset version:    9
Producer name:    pytorch
Producer version: 0.4
Domain:           
Model version:    0
Doc string:       
----------------------------------------------------------------
[11/20/2019-15:23:12] [V] [TRT] /home/jenkins/workspace/TensorRT/helpers/rel-6.0/L1_Nightly/build/source/parsers/onnxOpenSource/builtin_op_importers.cpp:773: Convolution input dimensions: (3, 112, 112)
[11/20/2019-15:23:12] [V] [TRT] /home/jenkins/workspace/TensorRT/helpers/rel-6.0/L1_Nightly/build/source/parsers/onnxOpenSource/builtin_op_importers.cpp:840: Using kernel: (3, 3), strides: (2, 2), padding: (1, 1), dilations: (1, 1), numOutputs: 64
[11/20/2019-15:23:12] [V] [TRT] /home/jenkins/workspace/TensorRT/helpers/rel-6.0/L1_Nightly/build/source/parsers/onnxOpenSource/builtin_op_importers.cpp:841: Convolution output dimensions: (64, 56, 56)
[11/20/2019-15:23:12] [V] [TRT] 8:Conv -> (64, 56, 56)
[11/20/2019-15:23:12] [V] [TRT] 9:BatchNormalization -> (64, 56, 56)
[11/20/2019-15:23:12] [E] [TRT] (Unnamed Layer* 3) [Parametric ReLU]: slope tensor must be unidirectional broadcastable to input tensor
[11/20/2019-15:23:12] [V] [TRT] 10:PRelu -> (0)
 ----- Parsing of ONNX model /home/ubuntu/temp_onnx/face_partial_upload.onnx is Done ---- 
[11/20/2019-15:23:12] [E] [TRT] (Unnamed Layer* 3) [Parametric ReLU]: slope tensor must be unidirectional broadcastable to input tensor
[11/20/2019-15:23:12] [E] Engine could not be created
&&&& FAILED TensorRT.trtexec # ./trtexec --onnx=/home/ubuntu/temp_onnx/face_partial_upload.onnx --saveEngine=/home/ubuntu/temp_onnx/face_partial_upload.trt --fp16 --batch=3 --verbose
```
