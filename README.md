Triangle
========

Upstream C language source for J. R. Shewchuk's Triangle mesh generator with modifications. Used by  [Triangle_jll.jl](https://github.com/JuliaBinaryWrappers/Triangle_jll.jl) which is at the core of [Triangulate.jl](https://github.com/JuliaGeometry/Triangulate.jl). 

See [README](README) for the original readme of the code.

Additions/modifications with respect to the upstram source found at [netlib/voronoi](https://netlib.org/voronoi):
- Replace `unsigned long` by ULONG to be flexible with this type. While in general, `unsigned long` is the right choice, on Windows (mingw32)
  it needs to be `unsigned long long`. Similar issue [here](https://github.com/libigl/triangle/pull/1). The requirement is that `ULONG` can hold a pointer.
- Longjump to caller replacing error exit.
- Support passing triangle sizing function from Julia.
