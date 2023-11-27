See [OpenAI Assistants API. Function Calling + Node.js](https://youtu.be/YTURKTxMaZE?si=kn8_zYMBddqhyA_K) by Mervin Praison

See also: <https://www.npmjs.com/package/yahoo-finance2>

Execution:

```
➜  assistant-function-mervin-praison git:(main) node index.mjs 
{
  id: 'run_UJO5Y34vCZJXJ8YqrwR6L0ns',
  object: 'thread.run',
  created_at: 1701121773,
  assistant_id: 'asst_mrGwfaE05ZXOOVN6XYKtpUpz',
  thread_id: 'thread_WY3ui3MW7uuzCNsTpYeF8Vv5',
  status: 'queued',
  started_at: null,
  expires_at: 1701122373,
  cancelled_at: null,
  failed_at: null,
  completed_at: null,
  last_error: null,
  model: 'gpt-4-1106-preview',
  instructions: 'Please address the user as Mervin Praison.',
  tools: [ { type: 'function', function: [Object] } ],
  file_ids: [],
  metadata: {}
}
{
  id: 'run_UJO5Y34vCZJXJ8YqrwR6L0ns',
  object: 'thread.run',
  created_at: 1701121773,
  assistant_id: 'asst_mrGwfaE05ZXOOVN6XYKtpUpz',
  thread_id: 'thread_WY3ui3MW7uuzCNsTpYeF8Vv5',
  status: 'requires_action',
  started_at: 1701121773,
  expires_at: 1701122373,
  cancelled_at: null,
  failed_at: null,
  completed_at: null,
  required_action: {
    type: 'submit_tool_outputs',
    submit_tool_outputs: { tool_calls: [Array] }
  },
  last_error: null,
  model: 'gpt-4-1106-preview',
  instructions: 'Please address the user as Mervin Praison.',
  tools: [ { type: 'function', function: [Object] } ],
  file_ids: [],
  metadata: {}
}
Requires action
[
  {
    id: 'call_NTk790iIRdMC7xt3iMqLRpmO',
    type: 'function',
    function: { name: 'getStockPrice', arguments: '{"symbol":"AAPL"}' }
  }
]
Fetching crumb and cookies from https://finance.yahoo.com/quote/AAPL...
fetch https://guce.yahoo.com/consent?brandType=nonEu&gcrumb=f6Zqiyk&done=https%3A%2F%2Ffinance.yahoo.com%2Fquote%2FAAPL
fetch https://consent.yahoo.com/v2/collectConsent?sessionId=3_cc-session_63beaa2d-7c6b-4776-888f-c3ef7b5d3767
fetch https://consent.yahoo.com/v2/collectConsent?sessionId=3_cc-session_63beaa2d-7c6b-4776-888f-c3ef7b5d3767
fetch https://guce.yahoo.com/copyConsent?sessionId=3_cc-session_63beaa2d-7c6b-4776-888f-c3ef7b5d3767&lang=es-ES
Fetching crumb and cookies from https://finance.yahoo.com/quote/AAPL?guccounter=1...
Success. Cookie expires on Infinity
New crumb: X2Rv97pOVWH
{
  id: 'run_UJO5Y34vCZJXJ8YqrwR6L0ns',
  object: 'thread.run',
  created_at: 1701121773,
  assistant_id: 'asst_mrGwfaE05ZXOOVN6XYKtpUpz',
  thread_id: 'thread_WY3ui3MW7uuzCNsTpYeF8Vv5',
  status: 'completed',
  started_at: 1701121787,
  expires_at: null,
  cancelled_at: null,
  failed_at: null,
  completed_at: 1701121789,
  last_error: null,
  model: 'gpt-4-1106-preview',
  instructions: 'Please address the user as Mervin Praison.',
  tools: [ { type: 'function', function: [Object] } ],
  file_ids: [],
  metadata: {}
}
Assistant: The current stock price of Apple (AAPL) is $189.79 USD.
User: What is the stock price of Apple?
Run is completed.
➜  assistant-function-mervin-praison git:(main)
```