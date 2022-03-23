# Technical_Challenge_Ília_!

Technical challenge performed for the Ília's selection process.


## Challenge:

- Enhance product service:
    *   [Delete product rpc call](https://github.com/LDeolindo/nameko-devex/blob/master/gateapi/gateapi/api/routers/product.py);
    *   [Wire into smoketest.sh](https://github.com/LDeolindo/nameko-devex/blob/master/test/nex-smoketest.sh);

- Enhance order service:
    *   [List orders rpc call](https://github.com/LDeolindo/nameko-devex/blob/master/gateapi/gateapi/api/routers/order.py);
    *   [Wire into smoketest.sh](https://github.com/LDeolindo/nameko-devex/blob/master/test/nex-smoketest.sh);

- Execute performance test:
    *   Question 1: Why is performance degrading as the test run longer?

    `R: Because the complexity level, amount of load and the number of users are increasing over time, making the system heavy, thus increasing resource usage and response time. Load X Resource X Performance. Response Time X Number of Users. Other times it's because the code is a little inefficient: with little amount of data being executed in X time, but as the load increases the time also, thereby code failure points end up being exposed. Sometimes even  the amount of resources used or even bad tests.`

    *   Question 2: How do you fix it?

    `R: Increasing processing and resource capacity. Trying to isolate parts of the test and running them separately in order to verify if the cause of the problem is in the writing of the test or product code, to try to make corrections and make the code perform better. `


## Challenge - Redone:
- Execute performance test:
    *   Question 1: Why is performance degrading as the test run longer?

    `R: The test performance is degrading with time because the number of threads (concurrency: 1) is lower compared with number of users (3), whats make high the levels of CPU and Memory when you increase the time.`

    *   Question 2: How do you fix it?

    `R: To fix this is necessary increase the number of threads, reducing the number of users by concurrency. When making some tests was found that the number of threads needed can be 300, 500 or 700, but searching the documentation they say to "Make sure you don't go over 75% CPU or 85% memory usage throughout the test", so whats make more sense is using 300.`
    
    *   (bonus): Fix it

    [Fixed!](https://github.com/LDeolindo/nameko-devex/blob/master/test/nex-bzt.yml);
