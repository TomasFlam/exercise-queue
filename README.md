# Multi-Producer Multi-Consumer Queue

Implement a multi-producer, multi-consumer priority queue in Python with
following features.
* Each inserted item has a priority associated with it.
  - If the inserted item already exists in the queue, its new priority is the
    sum of the old and the new priority.
  - When extracting, items with the highest priority are returned first.

* Other functionality (e.g. blocking, safe concurrent operations of multiple
  threads, etc.) is similar to that of `queue.Queue`.
  - Ideally, it is possible to use `PriorityQueue` instead of `queue.Queue` at any
    place without modifications of the code.

* Implement method
  `get_n(n: int, block: bool, timeout: Optional[float]) -> List[Item]`
  batching the results.
  - Queue blocks until at least `n` items are available (or timeout expires)
    and then return the gathered items.
