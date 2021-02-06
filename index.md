# Software ecology

npm, conda/pip and dependencies in general are the new fossil fuels.
They let us rapidly go forward and they will be the end of us.
If we don't pay attention to our solutions' dependecy trees and their depths,
what we're deploying is mostly pollution even if serves the moment's business purpose.

It's not hardware for a long long time anymore.
The moment we hit the Moore's limit, instead of actually addressing the problem,
we went the usual enterprise way of ignoring the problem and
"just put your SAP into an all-memory system".
Because it's hard accepting that we're writing software in languages that are single-core in their design and
philosophy.

We don't need supercomplex CPUs with speculative execution.
We need languages/paradigms that produce code which naturally scales to all available cores
(which don't need to be in the same CPU or even colocated hardware).
Making multicore a simple for `(i=0; i<100; i++) { sum +=i+1 }` is not trivial for a compiler/runtime, while `seq(0, 100).map(i=> i+1).sum()` is.