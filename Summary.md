1. Spark is batch processing, and Flink is continous processing, So Spark fits for log processing, and Flink is for real time processing
2. CDC relation with Database
3. Redis cache is single thread / atomic, Distributed Cache, pre computer store in redis
5. blob --> S3 --> CDN  presigned URL
6. large chunk 5-10MB, use hash identify, for resuming uploading, use S3 event update chunk status
7. streaming: real time process, pub sub, queue + FLink, event Queue (windowing)
8. GeoSpaical index: redis/  Elastic Search
9. High QPS: CDN, LB, Horizantal Scale
10. hot event : queue
11. Websocket: dual connection, use websocket manager if needs cross commute
12. dynamic config instead of static config
13. Database: optimal, compression, encrypt
14. Thinking careful use which protocal, SSE, webSocket, poll, long poll, webRTC
15. KAFKA : retry + exponiential back off
16. Cron Job for pre computer / cleanup quite useful at beginning . RT is complex and buggy
17. RT sorting, leaderboard, TopN : Redis sortedset with CDC, redis and DB update same time
18. read /write function separate
19. pub/sub with topic
20. batch call reduce frequency
21. TFIDF: word freq for search
22. cold storage
23. video, stream: transcode, different format
24. Pagination: with cache
25. Zookeeper control N replicas
26. 3rd party data source usage
27. Run Filtration then ranking --> two Stage Architecture
28. User Info host in Http header using JWT
29. Pubsub + WebSocket / SSE (consider how about poll) maybe no need for RT
30. Split data into Hot (cache) / warm (SSD / memory table)/ cold (S3)
31. Dynamic Partitions using Consistent hashing, rehashing, use Zookeeper control
32. Queue + Worker Combined
    1. Large scale of traffic
    2. Keep all transaction safe and not drop
34. Dynamic Horizontal Scale
35. Search: Pagination (page={} & pageSize= {} / Cursor={} & PageSize= {})
36. Producer + queue --> Real-time Processing	Event-driven systems
    1. Realtime logs, metrics, user activity tracking (e.g., Kafka)
    2. Decoupling services (e.g., microservices comms)
    3. Multiple consumers needed
37. Queue → Worker (Batch or Async) Background processing
    1. Sending emails/SMS
    2. Image processing
    3. Payment confirmation
    4. Any non-urgent or retry-prone task
