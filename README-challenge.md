# Desafio_Técnico_Ília_!

Desafio técnico realizados para o processo seletivo da Ília.


## Desafio prático:

- Enhance product service:
    *   [Delete product rpc call](https://github.com/LDeolindo/nameko-devex/blob/master/gateapi/gateapi/api/routers/product.py);
    *   [Wire into smoketest.sh](https://github.com/LDeolindo/nameko-devex/blob/master/test/nex-smoketest.sh);

- Enhance order service:
    *   [List orders rpc call](https://github.com/LDeolindo/nameko-devex/blob/master/gateapi/gateapi/api/routers/order.py);
    *   [Wire into smoketest.sh](https://github.com/LDeolindo/nameko-devex/blob/master/test/nex-smoketest.sh);

- Execute performance test:
    *   Question 1: Why is performance degrading as the test run longer?

    `R: Pois o nível de complexidade e quantidade de carga  vai aumentando com o tempo, deixando o sistema pesado, com isso aumentando o uso de recurso e tempo de respostas. E a quantidade de usuários vai aumentando. Carga X Desempenho e Tempo de Resposta X Número de Usuários. Outras vezes é pelo fato do código estar um pouco ineficiente, com pouca quantidade de dados execute em um tempo X, porém conforme a carga aumenta, pontos falhos do código acabam sendo expostos. Outras vezes a quantidade de recurso utilizado ou até mesmo testes malfeitos.`

    *   Question 2: How do you fix it?

    `R: Aumentando a capacidade de processamento e de recurso. Tentando isolar partes do teste e executando separadamente com a finalidade de verificando se a causa do problema é na escrita do código do teste ou do produto, para tentar realizar correções e deixar o código com uma performance melhor.`