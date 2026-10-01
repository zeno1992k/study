# Node.js 전체 목차

## 01. Node.js가 뭔지
1. Node.js 정의
2. JavaScript 런타임
3. ECMAScript와 Node API 구분
4. 브라우저 JS와 Node JS 차이
5. 호스트 환경
6. V8
7. libuv
8. 싱글 스레드 오해
9. 메인 스레드와 스레드 풀
10. 이벤트 루프
11. 블로킹 / 논블로킹
12. I/O 바운드
13. CPU 바운드
14. REPL
15. node 파일 실행
16. node -e
17. node --check
18. 버전 확인
19. process.versions
20. Current / LTS
21. nvm
22. 버전을 고정하는 이유

## 02. 이벤트 루프를 제대로
23. 콜스택
24. 힙
25. 태스크 큐
26. 마이크로태스크 큐
27. timers 단계
28. pending callbacks 단계
29. poll 단계
30. check 단계
31. close callbacks 단계
32. setTimeout
33. setInterval
34. setImmediate
35. process.nextTick
36. queueMicrotask
37. Promise then이 마이크로태스크인 이유
38. nextTick과 Promise 순서
39. setTimeout(0)이 0ms가 아닌 이유
40. 이벤트 루프를 막는 코드
41. 긴 JSON.parse
42. 긴 동기 루프
43. 블로킹을 찾는 감

## 03. 실행 환경 process
44. process 객체
45. process.argv
46. argv0
47. execArgv
48. process.env
49. 환경변수는 문자열
50. process.cwd
51. process.chdir
52. process.exit
53. 종료 코드
54. process.exitCode
55. beforeExit
56. exit
57. process.pid
58. process.ppid
59. process.title
60. stdin
61. stdout
62. stderr
63. stdin이 흐르지 않을 때 resume
64. 파이프와 TTY 차이
65. process.hrtime
66. process.uptime
67. process.memoryUsage
68. process.cpuUsage
69. process.resourceUsage
70. NODE_ENV
71. .env 파일과 실제 환경변수 차이
72. 전역 global
73. globalThis
74. __dirname
75. __filename
76. ESM에서 import.meta.url
77. ESM에서 디렉터리 경로 얻기

## 04. 모듈 시스템
78. 모듈이 필요한 이유
79. CommonJS
80. require
81. require 캐시
82. require.resolve
83. module.exports
84. exports와 module.exports 차이
85. 순환 참조가 CJS에서 어떻게 깨지는지
86. ES Modules
87. import
88. export
89. default export
90. named export
91. import() 동적 import
92. top-level await
93. package.json type
94. .cjs
95. .mjs
96. .js가 CJS인지 ESM인지
97. CJS에서 ESM 부르기
98. ESM에서 CJS 부르기
99. module.createRequire
100. 내장 모듈
101. node: 접두사
102. 로컬 파일 모듈
103. 서드파티 모듈
104. 모듈 해석 순서
105. node_modules를 위로 찾아 올라가는 규칙
106. package exports
107. package imports
108. exports의 import / require 조건
109. main 필드
110. bin 필드
111. files 필드

## 05. 패키지와 npm
112. package.json
113. name
114. version
115. private
116. scripts
117. dependencies
118. devDependencies
119. peerDependencies
120. optionalDependencies
121. npm init
122. npm install
123. npm install 패키지
124. npm uninstall
125. npm update
126. npm ls
127. npm ci
128. install과 ci 차이
129. package-lock.json
130. lock 파일을 커밋하는 이유
131. node_modules
132. semantic versioning
133. ^
134. ~
135. 정확한 버전
136. latest
137. tag
138. npx
139. npm run
140. pre / post 스크립트
141. 전역 설치
142. 로컬 설치
143. PATH와 로컬 bin
144. .npmrc
145. 스코프 패키지
146. engines
147. overrides
148. workspaces
149. corepack
150. pnpm / yarn을 나중에 보는 이유
151. npm audit의 한계
152. 패키지를 직접 공개하는 개념

## 06. 경로
153. path 모듈
154. path.join
155. path.resolve
156. join과 resolve 차이
157. path.normalize
158. path.relative
159. path.basename
160. path.dirname
161. path.extname
162. path.parse
163. path.format
164. path.sep
165. path.delimiter
166. path.posix
167. path.win32
168. 절대 경로
169. 상대 경로
170. .. 경로 탈출
171. Windows 경로를 코드에서 다루기

## 07. 파일 시스템
172. fs가 웹 API가 아닌 이유
173. 콜백 fs
174. 동기 fs
175. fs/promises
176. 동기 API를 서버에서 피해야 하는 이유
177. readFile
178. writeFile
179. appendFile
180. open
181. close
182. FileHandle
183. read
184. write
185. flag
186. encoding을 빼면 Buffer
187. existsSync를 믿으면 안 되는 이유
188. access
189. stat
190. lstat
191. 파일과 디렉터리 구분
192. mkdir
193. recursive
194. readdir
195. withFileTypes
196. opendir
197. rm
198. rmdir
199. unlink
200. rename
201. cp
202. copyFile
203. symlink 개념
204. readlink
205. chmod
206. 권한 비트
207. truncate
208. watch
209. watch는 플랫폼마다 다름
210. glob
211. 임시 파일
212. 원자적 교체 개념
213. ENOENT
214. EACCES
215. EEXIST
216. 에러 코드로 분기

## 08. Buffer와 바이너리
217. Buffer가 필요한 이유
218. Buffer.from
219. Buffer.alloc
220. Buffer.allocUnsafe
221. allocUnsafe가 위험한 이유
222. Buffer.concat
223. 길이
224. 인덱스
225. subarray
226. slice가 예전과 다른 점
227. utf8
228. base64
229. base64url
230. hex
231. latin1
232. 문자열로 바꾸기
233. readUInt8 / readUInt32BE
234. write
235. 엔디언
236. TextEncoder
237. TextDecoder
238. 잘못된 인코딩
239. Buffer 풀

## 09. 스트림
240. 스트림 개념
241. Readable
242. Writable
243. Duplex
244. Transform
245. PassThrough
246. flowing 모드
247. paused 모드
248. data
249. end
250. finish
251. readable 이벤트
252. read()
253. push
254. pipe
255. pipeline
256. finished
257. backpressure
258. highWaterMark
259. objectMode
260. for await로 스트림 읽기
261. createReadStream
262. createWriteStream
263. 대용량 파일
264. 스트림 에러
265. pipeline이 pipe보다 나은 이유
266. 웹 스트림과 Node 스트림
267. 둘 사이 변환
268. 압축 스트림 zlib

## 10. 이벤트
269. EventEmitter
270. on
271. once
272. emit
273. off
274. removeListener
275. removeAllListeners
276. prependListener
277. 동기 호출이라는 점
278. error 이벤트를 안 들으면 죽음
279. 최대 리스너
280. 메모리 누수 경고
281. 이벤트 이름
282. 인자 전달
283. this 바인딩
284. 커스텀 이벤트 설계
285. EventTarget과 EventEmitter 차이

## 11. 타이머와 취소
286. setTimeout
287. clearTimeout
288. setInterval
289. clearInterval
290. 인터벌이 겹치는 경우
291. setImmediate
292. clearImmediate
293. timers/promises
294. setTimeout promise
295. AbortController
296. AbortSignal
297. AbortSignal.timeout
298. 취소 가능한 비동기 작업
299. 요청이 끊기면 작업 취소

## 12. 비동기 패턴
300. 에러 우선 콜백
301. 콜백을 두 번 호출하면 안 되는 이유
302. 콜백 지옥
303. promisify
304. Promise
305. async / await
306. 동기 throw
307. rejected promise
308. await 빼먹기
309. forEach 안에서 await
310. for...of 순차 실행
311. Promise.all
312. Promise.allSettled
313. Promise.race
314. Promise.any
315. 병렬과 순차
316. 동시성 제한
317. unhandledRejection
318. uncaughtException
319. uncaughtExceptionMonitor
320. 프로세스를 살릴지 죽일지

## 13. 에러
321. Error
322. message
323. stack
324. cause
325. 커스텀 에러
326. 에러 코드 code
327. syscall
328. 운영 에러
329. 프로그래머 에러
330. 예상 가능한 실패
331. 복구 가능한 실패
332. 로깅 후 종료
333. 에러를 삼키면 안 되는 곳
334. 도메인 에러와 HTTP 상태 매핑

## 14. console과 로그
335. console.log
336. console.error
337. console.warn
338. time / timeEnd
339. console.log는 디버그용
340. stdout과 stderr 나누기
341. 로그 레벨
342. 구조화 로그
343. JSON 로그
344. 요청 아이디
345. 시크릿을 로그에 안 남기기

## 15. HTTP 서버
346. HTTP 메시지
347. 시작줄
348. 헤더
349. 본문
350. 메서드
351. 상태 코드
352. http.createServer
353. IncomingMessage
354. ServerResponse
355. req.method
356. req.url
357. req.headers는 소문자
358. host
359. socket
360. res.statusCode
361. res.setHeader
362. res.writeHead
363. res.write
364. res.end
365. writeHead 이후 헤더 수정 불가
366. Content-Type
367. Content-Length
368. chunked
369. req.on('data')
370. 본문을 Buffer로 모으기
371. JSON 파싱
372. 본문 크기 제한
373. URL 파싱
374. 쿼리스트링
375. WHATWG URL
376. 라우팅을 직접 나누기
377. 404
378. 405
379. 정적 파일
380. 경로 탈출 막기
381. redirect
382. Server timeout
383. headersTimeout
384. requestTimeout
385. 연결 유지 keep-alive
386. http.Agent
387. 서버에서 나가는 요청
388. 클라이언트 타임아웃

## 16. fetch와 HTTPS
389. Node 전역 fetch
390. undici
391. fetch와 http.request 차이
392. Request / Response
393. 헤더 객체
394. res.ok
395. res.json
396. res.text
397. 스트림 응답
398. AbortSignal로 fetch 취소
399. https 모듈
400. TLS 개념
401. 인증서
402. NODE_TLS_REJECT_UNAUTHORIZED를 끄면 안 되는 이유
403. HTTP/2 개념
404. http2 모듈이 따로 있는 이유

## 17. 웹 서버에서 만나는 개념
405. REST
406. 리소스
407. JSON API
408. 상태 코드 고르기
409. 검증
410. 400과 422
411. 401과 403
412. CORS는 브라우저 정책
413. 서버가 CORS 헤더를 붙여 주는 이유
414. preflight
415. 쿠키
416. Set-Cookie
417. HttpOnly
418. Secure
419. SameSite
420. 세션
421. 토큰
422. 인증
423. 인가
424. 미들웨어 개념
425. 요청 생명주기
426. body를 한 번만 읽는 이유
427. 파일 업로드
428. multipart
429. 경계 문자열
430. SSRF 개념
431. 신뢰하면 안 되는 호스트 헤더

## 18. 프레임워크를 보기 전에
432. 프레임워크가 감추는 것
433. Express가 얇은 이유
434. 라우터
435. 미들웨어 체인
436. next
437. 에러 미들웨어 시그니처
438. 정적 미들웨어
439. 프레임워크 없이 같은 구조
440. Fastify
441. Nest
442. 프레임워크를 고르기 전에 코어를 보는 이유

## 19. TCP와 기타 네트워크
443. net 모듈
444. TCP 서버
445. Socket
446. data / end / close
447. 바이트 스트림이라 메시지 경계가 없음
448. 프레임 나누기
449. dgram
450. UDP 개념
451. dns
452. dns.lookup과 dns.resolve 차이
453. 타임아웃
454. 소켓 에러
455. ECONNREFUSED
456. ETIMEDOUT
457. EPIPE

## 20. 자식 프로세스
458. child_process가 필요한 때
459. exec
460. execFile
461. spawn
462. fork
463. 쉘을 켜는 API와 안 켜는 API
464. 명령 주입
465. stdio
466. stdout 버퍼가 꽉 차면 멈춤
467. 종료 코드
468. 시그널로 죽은 경우
469. IPC 채널
470. 부모와 메시지
471. 자식 좀비 / 대기

## 21. 워커와 클러스터
472. worker_threads
473. 메인 스레드와 워커
474. postMessage
475. 구조적 복제
476. transferList
477. MessageChannel
478. CPU 작업을 워커로
479. 워커는 I/O 마법이 아님
480. SharedArrayBuffer 개념
481. cluster
482. 같은 포트를 여러 프로세스가
483. 라운드 로빈 개념
484. 프로세스 간 메모리는 안 공유
485. 스케일 아웃과 클러스터 차이

## 22. 암호와 랜덤
486. crypto
487. 해시
488. createHash
489. sha256
490. hex digest
491. hmac
492. randomBytes
493. randomUUID
494. timingSafeEqual
495. 비밀번호를 일반 해시만으로 저장하면 안 되는 이유
496. scrypt / pbkdf2 개념
497. 전역 crypto와 node:crypto
498. 타이밍 공격 개념

## 23. 자주 쓰는 코어 유틸
499. os
500. cpus
501. totalmem
502. freemem
503. hostname
504. tmpdir
505. EOL
506. util.promisify
507. util.types
508. util.format
509. inspect
510. querystring은 레거시
511. URLSearchParams
512. readline
513. readline/promises
514. zlib
515. gzip
516. assert
517. assert/strict
518. perf_hooks
519. AsyncLocalStorage
520. 요청 단위 컨텍스트
521. diagnostics_channel 개념
522. v8 힙 통계 개념
523. vm은 샌드박스가 아님
524. node:sqlite가 생긴 배경
525. node:test

## 24. 테스트
526. 단위 테스트
527. 통합 테스트
528. node:test
529. describe
530. it
531. assert
532. mock
533. mock timers
534. 비동기 테스트가 끝나야 함
535. 열린 핸들 때문에 테스트가 안 끝남
536. 포트 0으로 바인딩
537. 임시 디렉터리
538. 픽스처
539. HTTP 핸들러만 테스트
540. 커버리지 개념

## 25. 디버깅과 진단
541. 스택 읽기
542. 원인 체인 따라가기
543. node inspect
544. --inspect
545. Chrome DevTools로 붙기
546. 브레이크포인트
547. NODE_DEBUG
548. --trace-warnings
549. 경고를 에러로
550. 메모리 스냅샷 개념
551. CPU 프로파일 개념
552. 이벤트 루프 지연 측정
553. 재현 절차 만들기

## 26. 설정, 시그널, 종료
554. 설정을 코드와 분리
555. 개발 / 테스트 / 운영
556. 시크릿
557. 포트
558. 호스트 0.0.0.0과 127.0.0.1
559. SIGINT
560. SIGTERM
561. SIGHUP
562. graceful shutdown
563. 새 요청 거부
564. 기존 연결 대기
565. 타임아웃 후 강제 종료
566. beforeExit만 믿고 정리하면 안 되는 이유

## 27. 성능
567. 뭐가 느린지 먼저 재기
568. 동기 fs
569. 큰 파일 readFile
570. 큰 JSON
571. 이벤트 루프 블로킹
572. 스트림으로 바꾸기
573. 불필요한 await 순차
574. 커넥션을 매번 새로 열기
575. Agent keep-alive
576. 클러스터로 코어 쓰기
577. GC를 먼저 만지지 않기
578. Number 안전 정수
579. BigInt가 JSON에 안 들어가는 문제

## 28. 보안
580. 입력 검증
581. 경로 탈출
582. 명령 주입
583. 프로토타입 오염
584. ReDoS 개념
585. 의존성 신뢰
586. 락파일
587. 시크릿 커밋 금지
588. Rate limit 개념
589. 본문 크기 제한
590. 헤더 크기 제한
591. 보안 헤더 개념
592. 디렉터리 리스팅 금지
593. 권한 모델 --permission 개념

## 29. 데이터 저장은 Node 밖
594. Node는 DB가 아님
595. 파일 저장의 한계
596. SQL / NoSQL
597. 드라이버
598. 커넥션 풀
599. 쿼리와 HTTP 핸들러 분리
600. 트랜잭션은 DB 책임
601. N+1 개념
602. 마이그레이션
603. 캐시
604. 재시도
605. 타임아웃을 DB 호출에도

## 30. CLI로 쓸 때
606. 쉬뱅
607. 실행 권한
608. argv 파싱
609. 도움말
610. stdout에 결과
611. stderr에 에러
612. 종료 코드 규약
613. 파이프 입력
614. bin 필드와 npm link 개념

## 31. TypeScript와 실행
615. Node는 원래 TS 런타임이 아님
616. 타입은 지워진다
617. 트랜스파일
618. tsx / ts-node는 도구
619. @types/node
620. 최신 Node의 타입 스트립 개념
621. ESM과 모듈 해석
622. 경로 alias는 런타임이 모름

## 32. 배포 전에
623. 엔트리
624. npm start
625. 프로세스 매니저 개념
626. 환경변수 주입
627. 헬스체크
628. 로그는 stdout
629. PID 1
630. 컨테이너에서 시그널
631. 빌드가 필요한 경우
632. 소스맵
633. node --watch
634. 운영에서 watch를 켜지 않음

## 33. 자주 깨지는 것
635. CJS와 ESM을 섞다 죽음
636. __dirname이 ESM에 없음
637. 확장자 누락
638. exports 맵에 경로가 없음
639. await 누락
640. forEach + async
641. 에러를 빈 catch로 삼킴
642. 콜백과 Promise를 같이 완료
643. 본문을 두 번 읽기
644. JSON이 아닌데 JSON.parse
645. 헤더를 end 이후에 설정
646. 포트 점유 EADDRINUSE
647. CORS를 서버 크래시로 착각
648. Windows 경로 구분자
649. exists 체크 후 생성 사이의 경합
650. 큰 파일 readFile로 메모리 폭발
651. 동기 함수로 이벤트 루프 정지
652. 테스트 포트 충돌
653. 핸들을 안 닫아 프로세스가 안 죽음
654. 환경변수 "false"가 참처럼 쓰임
655. 자식 프로세스 쉘 인젝션
656. allocUnsafe로 쓰레기 바이트 유출
657. error 이벤트 미처리로 프로세스 종료
658. 워커에 함수를 그냥 넘길 수 없음
659. cluster에서 메모리 공유라고 착각
660. fetch 실패와 HTTP 4xx를 같은 것으로 착각
