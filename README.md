# UrsineMath
UrsineMath is a small linear math library with SIMD (Single Instruction Multiple Data) optimizations.  It is a research project at heart, and is still very much so a work in progress.

Features Include:
- SSE4.1 intrinsics and below
- Vector, Matrix, Quaternion classes
- Extensive (and redundant at times) test suite

These math libraries served as great learning resources and sources of inspiration:
- https://github.com/bulletphysics/bullet3/tree/master/src/LinearMath
- http://clb.demon.fi/MathGeoLib/nightly/
- https://msdn.microsoft.com/en-us/library/windows/desktop/hh437833(v=vs.85).aspx

Target Platforms:
- Windows (MSVC)
- OS X & Linux (GCC/Clang)
