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
17. RT soring, leaderboard, TopN : Redis sortedset with CDC
18. read /write functoin separate
19. pub/sub with topic
20. batch call reduce frequency
21. TFIDF: word freq for search
22. cold storage
23. video, stream: transcode, different format
24. Pagination: with cache
