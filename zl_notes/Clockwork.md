# Clockwork

2023.4.12 by Liang

## Useful sentences
- With an explicit focus on the
ubiquitous deep neural network (DNNs) architectures we firs
show that DNN inference is fundamentally a deterministic
sequence of mathematical operations that has a predictable
execution time on a GPU. (From Introduction)
- Model serving: the model serving users (customers
or internal applications) upload their pre-trained DNN
ahead of time (the natural format for which is ONNX/NNEF).
Their applications can then submit inference requests to an
API. The model serving back-end manages the users’ models
and the hardware accelerator resources, and provides timely
responses to inference requests. Upon receiving an inference
request, it loads the appropriate model into hardware if not
already loaded, runs the DNN on the input, and returns the
resultingoutputtotheuser. (From background and motivation)
- DNN inference is predictable：The 99.99th
percentile latency was within 0.03% of the median latency. （Figure 2a, From motivation/observation）

## Challenges and Solutions for predictable inference 
- C1: Managed memory and caches can be unpredictable
    - Solution: Clockworktreats GPU memory as a cache, letting commonly or recently used models avoid
expensive loads. To overcome C1, workers explicitly expose
LOAD and UNLOAD actions to the controller for copying
models to and removing models from worker’s GPU memory
with deterministic latency. These actions also update the state
that the controller tracks for the worker.

- C2: Hardware interactions can be unpredictable
    - Solution: Clockwork workers therefore run a single EXEC at a time, a design choice that reduces performance variability by two orders of magnitude while only minimally decreasing inference throughput

- C3: External factors can trigger performance variance (performance interference through shared
network bottlenecks, thermal throttling of CPUs and GPUs,
and others)
    - Solution: Clockworkworkersreceive
LOAD, UNLOAD, and INFER actions from the controller with
detailed timing expectations attached: earliest and latest timestamps. Actions that cannot start within the prescribed window are cancelled and never execute. This allows workers to quickly get back on schedule after an individual action is delayed unexpectedly (C3) by skipping one or more actions, minimizing the impact of the delay on other actions.
