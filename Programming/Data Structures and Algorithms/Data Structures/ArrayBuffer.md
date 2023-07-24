## What is it?
- also known as RingBuffer
- like an [[ArrayList]] but without head being length and tail being zero
- you now don't have to shift everything to remove the head you can just head + 1
- it is a ring so it can go from the end to the front
- if tail exceeds head, you need to resize and it becomes harder
- 