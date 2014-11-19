1. <a href="http://www.cs.cmu.edu/~jfineman/sbtree.pdf">Michael A. Bender, Martin Farach-Colton, Jeremy T. Fineman, Yonatan R. Fogel, Bradley C. Kuszmaul, Jelani Nelson Cache-Oblivious Streaming B-trees</a>

  A streaming B-tree is a dictionary that efficiently implements insertions and range queries. We present two cache-oblivious streaming B-trees, the shuttle tree, and the cache-oblivious lookahead array (COLA).
  For block-transfer size B and on N elements, the shuttle tree implements searches in optimal O(log B+1N) transfers, range queries of L successive elements in optimal O(log sup(B+1) N +L/B) transfers, and insertions in O((log sup(B+1) N)/B^Θ(1/(log log B)^2)+(log^2N)/B) transfers, which is an asymptotic speedup over traditional B-trees if B ≥ (log N)^(1+c/log log log^2 N) for any constant c >1.
  
  A COLA implements searches in O(log N) transfers, range queries in O(log N + L/B) transfers, and insertions in amortized O((log N)/B) transfers, matching the bounds for a (cache-aware) buffered repository tree. A partially deamortized COLA matches these bounds but reduces the worst-case insertion cost to O(log N) if memory size M = Ω(log N). We also present a cache-aware version of the COLA, the lookahead array, which achieves the same bounds as Brodal and Fagerberg's (cache-aware) Bε-tree.
  
  We compare our COLA implementation to a traditional B-tree. Our COLA implementation runs 790 times faster for random inser-tions, 3.1 times slower for insertions of sorted data, and 3.5 times slower for searches.

