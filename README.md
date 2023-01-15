# Neural3DReconstruction.jl

(Code to be released by mid-February 2023)

This package provides two major pieces of functionality:
1. NeRF[[1]](#1) and related models translated to Julia
2. Pipelines to take collections of 2D images and generate state-of-the-art 3D reconstructions

## Why?

NeRF (Neural Radiance Fields) and related neural network 3d reconstruction methods have exploded in capability and popularity in the last few years.  These networks learn the 3D structure, lighting, coloring, and other features of a scene primarily using as input 2D images and the poses of these images.

This package aims to make many of these approaches easily accessible and customizable in Julia.  Traditionally, going from a collection of 2D images to a dense 3D model using these state-of-the-art neural networks would require a complex pipeline spanning a number of applications and programming languages.  Julia is uniquely capable of handling all stages of the pipeline and thus allows for experimentation at every level.

## Related Packages
### Currently Used
- [Caesar.jl](https://github.com/JuliaRobotics/Caesar.jl) used for determining camera poses
- [Flux.jl](https://github.com/FluxML/Flux.jl) used for defining neural networks
- [CUDA.jl](https://github.com/JuliaGPU/CUDA.jl) used for custom kernels needed to improve training speed

### Future Integrations and Related
- [Flux3D.jl](https://github.com/FluxML/Flux3D.jl) reusable and common utilities and data structures for 3D deep learning.
(as logic and functions in Neural3DReconstruction.jl mature, we may move them to Flux3D.jl).
- [model-zoo](https://github.com/FluxML/model-zoo) variety of reusable neural network models (we may move some models from Neural3DReconstruction.jl to model-zoo over time)
- [RayTracer.jl](https://github.com/avik-pal/RayTracer.jl) differentiable ray tracing

## References
<a id="1">[1]</a>
Ben Mildenhall; Pratul P. Srinivasan; Matthew Tancik; Jonathan T. Barron Ravi Ramamoorthi; Ren Ng. "NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis". ECCV.