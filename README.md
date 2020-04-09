
National Science Foundation 
Research Experience for Undergraduates
Washington University in St. Louis
Big Data Focus

Researchers: Ulysses Butler and Joseph Li
Advisors: Dr. Jeremy Buhler and Dr. Roger Chamberlain

Data preprocessing is becoming increasingly important. Algorithms often require data input to be in a specific format. In this research, we examine how to efficiently transform graph data from an edge list to Compressed Sparse Row (CSR) representation. Notably, we are considering data sets on the scale of terabytes of data—too large to fit into RAM, thus necessitating data handling on the disk drive. Aware of the resulting bottleneck on performance speed, we minimize the number of file read and write operations whenever possible.

The data conversion is essentially performed with a sort on the edge list before its transformation to CSR format. This is implemented both sequentially and in parallel. The sequential version is done in C++ (intended for CPUs), whereas the parallel version is written in C using the OpenCL library (portable to GPUs and Multicore processors). In the parallel conversion, we integrate techniques such as the parallel prefix sum.

Subjected to timing tests, the sequential implementation yielded substantially faster results than the parallel version. Contrary to expectations, this result can be attributed to unoptimized code and the additional bottleneck of reading and writing to a GPU’s global memory.

While GPUs and related computing devices continue to be exploited for parallel computations, we have yet to fully grasp the underpinnings of speed improvements. Meanwhile, continual GPU advancements will likely close the occasional performance speed gap between parallel algorithms and their sequential counterparts.
