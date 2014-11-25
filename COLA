The basic COLA (cache oblivious lookahead array) datastructure is a series of arrays of exponentially growning size. The i_th array stores 2_i elements in sorted order. The arrays are stored sequentially.

To query the datastructure we perform a binary search in each array. This takes log(N/B) IOs per array. However, the first log(B) arrays can be searched in O(1) IOs. This means a query can be executed with log(N/B) · (log(N) − log(B)) = (log(N/B))^2 IOs. 

Insertion proceeds as follows. If the first array is empty, we insert into it. If not, we empty the first array and insert both elements into the next array if that is empty. If the second 1array is full, we empty it and try inserting all four elements into the third array and so on. In the end, we fill the first empty array by merging the insert with all preceeding arrays. 
For now, assume M/B >~ log(N). The cost of a merge is O(number of items merged/B) IOs. Each item participates in at most log N − log B non-free merges. (We don’t count merges involving the first O(log B) arrays as these can happen in memory.) If we imagine each item being given O(log(N/B)/B) ‘credits’ upon insertion and decucting O(1/B) credits when it participates in a 
merge, we see that the total number of IOs is O(N/B * log(N/B)). Thus the amortized cost of an insert is O((log(N/B))/B).

Removing the Assumption We assumed that M/B & log(N). This is necessary for merge to run efficiently. This can be removed for a constant factor increase in space usage. The idea is to break up the merging of log(N) arrays into pairwise merges. We start by merging the inserted item with the first array into a buffer. Then merge the second array with the buffer into another buffer and so on until everything has been merged.

1. <a href="http://people.seas.harvard.edu/~minilek/cs229r/lec/lec23.pdf">Jelani Nelson Algorithms for Big Data. Lec. 23: Cache-Oblivious Lookahead Array (COLA)</a>
