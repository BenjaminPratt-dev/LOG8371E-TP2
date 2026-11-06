CLAIM CARD
  Operation        : POST /realms/perf/protocol/openid-connect/token
  Workload         : 10 users, think time: between 0.1 and 0.3 s, duration: 35s, cache state: cold for first run, then warm for subsequent
  Statistic        : 
  run 1: "p50": 470.10956, "p95": 554.5901456, "p99": 1335.2377859599999 / mean: 489.5194989417249,  / error rate: 0% , linear interpolation at (n-1)*p 
  run 2: "p50": 466.922907, "p95": 540.5520675, "p99": 1316.7524524999994 / mean: 481.5149955452436 / error rate: 0% , linear interpolation at (n-1)*p
  run 3: "p50": 441.825977, "p95": 531.581328, "p99": 911.4382125999902 / mean: 453.7677803429844 / error rate: 0% , linear interpolation at (n-1)*p
  n observed       : 429, 431, 449
  Threshold        : maximum 1 failure per 1000 requests
  Decision rule    : ship if threshold stands, hold if exceeds, decided by Benjamin Pratt
  Limitation       : IID request bootstrap does not capture temporal dependence or host uncertainty
