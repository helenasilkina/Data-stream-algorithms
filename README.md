Streaming algorithms are algorithms for processing data streams in which the input is presented as a sequence of items and can be examined in only a few passes (typically just one). These algorithms have limited memory available to them (much less than the input size) and also limited processing time per item.

The field of streaming algorithms was first formalized and popularized in a paper by Noga Alon, Yossi Matias, and Mario Szegedy[1].

The performance of an algorithm that operates on data streams is measured by three basic factors:
    The number of passes the algorithm must make over the stream.
    The available memory.
    The running time of the algorithm.
  
In the data stream model, some or all of the input data that are to be operated on are not available for random access from disk or memory, but rather arrive as one or more continuous data streams. Streams can be denoted as an ordered sequence of points (or "updates") that must be accessed in order and can be read only once or a small number of times. 

1. <a href="http://www.vldb.org/conf/2001/P079.pdf">Gilbert, A. C.; Kotidis, Y.; Muthukrishnan, S.; Strauss, M. J. (2001), Surfing Wavelets on Streams: One-Pass Summaries for Approximate Aggregate Queries</a>
