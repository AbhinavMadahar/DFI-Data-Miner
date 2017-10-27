# Deep Frame Interpolation Data Miner

This is the program that processes YouTube videos returned from a particular search query into individuals scenes of greyscale frames.

It is being developed for the Deep Frame Interpolation project by Rutgers IEEE ML/AI.

## Algorithm Overview
The algorithm for deciding if a frame is the new frame in a scene is described as such.

Let F be a series mxn matrix of uint8 values describing a video such that F[i] is the ith frame of the video.
Let g be a function that maps mxn matrices to a real value. Let threshold be a real value. 

Then, a particular frame F[t] is the first frame of a new scene if and only if
```
g(F[t] - F[t-1]) >= threshold
```

We must define g and threshold in such a way that the previous condition is met.
We will decide how to define g and threshold after reviewing the literature.

## License

MIT License

Copyright (c) 2017 Abhinav Madahar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

