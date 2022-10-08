Triangle
========

Upstream C language source for J. R. Shewchuk's Triangle mesh generator with modifications. Used by  [Triangle_jll.jl](https://github.com/JuliaBinaryWrappers/Triangle_jll.jl) which is at the core of [Triangulate.jl](https://github.com/JuliaGeometry/Triangulate.jl). 

See [README](README) for the original readme of the code.

Additions/modifications with respect to the upstram source found at [netlib/voronoi](https://netlib.org/voronoi):
- Replace `unsigned long` by `unsigned long long` to be save on on systems where the former is 4 bytes only. Similar issue [here](https://github.com/libigl/triangle/pull/1).
- Longjump to caller replacing error exit
- Support passing triangle sizing function from Julia
