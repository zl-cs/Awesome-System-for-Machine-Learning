# ORLOJ
## Motivation
Dynamic DNNs can adapt their structures or parameters to the input during inference and are thus inherently data-dependent. Request execution times on dynamic DNNs come from a distribution
instead of being a single constant. Existing systems fail to capture
the high variance in incoming requests' execution times, and
when they batch multiple requests together, one long request
in the batch slows down many short ones, leading to large
number of SLO misses. 

## Challenges and Solutions
- C1: Batching ignores individual request's execution time
    - Solution: ORLOJ proposes a batch-aware priority score that derives batch execution time distributions given those of individual
requests, and uses the score to guide its batching decisions

- C2: Joint distribution of requests from different applications can be multimodal with even higher variance
    - Solution: ORLOJ tags each request
with its originating application and relies on probability theory
to accurately estimate batch execution times even when
execution times of requests in the same batch follow different
distributions.

## Results
In comparison to Clockwork [18],
Nexus [49], and Clipper [10], ORLOJ can improve the finish
rate when serving dynamic DNNs by 51–80% under tight
SLO constraints, and over 100% under more relaxed SLO settings.
For well-studied static DNN workloads, ORLOJ keeps
comparable performance with the state-of-the-art.

## Useful sentence
- The overall objective
of a model serving system can, therefore, be described as
maximize throughput while reducing SLO misses.
- Examples of dynamic
DNNs include various language models [12, 52] as well as
early-exit techniques used in emerging CNN models [53].

