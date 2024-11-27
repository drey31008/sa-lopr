# sa-lopr
algoritmo "Estrategia_de_Vendas"
var
    metaVendas, totalProdutos, precoProduto, vendasNecessarias, totalArrecadado: real
    i, qtdProdutos: inteiro
inicio
    escreval("=== Planejamento de Estratégia de Vendas ===")
    escreval("Informe a meta de vendas (em R$):")
    leia(metaVendas)
    escreval("Informe a quantidade de produtos disponíveis:")
    leia(qtdProdutos)
   totalProdutos <- 0
    vendasNecessarias <- 0
    para i de 1 ate qtdProdutos faca
        escreval("Informe o preço do produto ", i, " (em R$):")
        leia(precoProduto)
        totalProdutos <- totalProdutos + precoProduto
    fimpara
    se totalProdutos > 0 entao
        vendasNecessarias <- metaVendas / (totalProdutos / qtdProdutos)
    fimse
    escreval("=== Resultado da Estratégia de Vendas ===")
    escreval("Meta de vendas: R$", metaVendas:0:2)
    escreval("Total arrecadado: R$", totalArrecadado:0:2)

    escreval("=== Status fim===")
    escreval("Você precisa vender pelo menos ", vendasNecessarias:0:2, " produtos para atingir a meta.")
    se vendasNecessarias > qtdProdutos entao
        escreval("Alerta: A quantidade de produtos disponíveis é insuficiente para atingir a meta!")
        escreval("Sugestão: Reavaliar preços ou aumentar a disponibilidade de produtos.")
    senao
        escreval("Com a estratégia atual, é possível atingir a meta.")
    fimse

    escreval("=== Fim da Estratégia ===")
fimalgoritmo
