HYPOTHESIS
  Suspect            : Authenticating on every request is a large contributor to latency
  Predicted signal   : When increasing user count, Keyclock CPU usage should rise while PostgreSQL CPU stays stable
  Intervention       : Keep the token in cache for every request, reducing latency while user count increases
  Falsifier          : Keyclock CPU usage does not increase heavily with the increase in users

