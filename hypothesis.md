HYPOTHESIS
  Suspect            : Authenticating on every request is a large contributor to latency
  Predicted signal   : When increasing user count, Keyclock CPU usage should rise while PostgreSQL CPU stays stable
  Intervention       : Keep the token in cache for every request, reducing latency while user count increases
  Falsifier          : Keyclock CPU usage does not increase heavily with the increase in users

Validation: 

10 users: Keycloack average CPU usage: 700%, Postgres: 8%

20 users: Keycloack: 800%, Postgres: 8% 

CPU usage for keycloack increases significantly while Postgres stayed stable, confirming hypothesis.