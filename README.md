## Limiting-middleware

This module enforces limits based on IPs for you express APIs. So far, the usage is for my personal projects. But if there is interest, I could prioritize development for new features:

 * Better instantiation (pass in limits through a time-based DSL)
 * Improved logging
 * And more

### Import the module

```
npm i limiting-middleware --save
```

### Usage
```
const LimitingMiddleware = require('limiting-middleware');
app.use(new LimitingMiddleware({ limit: 100, resetInterval: 1200000 }).limitByIp());
// 100 request limit. 1200000ms reset interval (20m).
```
