# Resolução do Lab: Static Routing - Practice Exam Question 1

## Explicação

Este laboratório testa sua capacidade de **prever o comportamento da rede** com base nas rotas estáticas configuradas e no estado das interfaces. A chave para entender este cenário está em analisar o que acontece quando o link entre R1 e R2 falha (simulado com `shutdown` na interface Ethernet 0/1).

## Análise das Rotas

Quando a interface Ethernet 0/1 do R1 entra em estado de shutdown:
- A rota estática que aponta para o next-hop através dessa interface **não é removida automaticamente** do R1
- No entanto, o next-hop torna-se **inalcançável** (not reachable)
- O roteador R1 precisa encontrar outras rotas válidas para os destinos

## Comportamento Esperado

Após a falha do link R1-R2:

- **Para o Servidor S1** (192.168.10.0/24): Os pacotes são encaminhados via R1 -> R3, pois esta é a rota estática alternativa válida.
- **Para o Servidor S2** (192.168.20.0/24): Os pacotes são descartados porque não existe uma rota estática válida alternativa após a falha do link direto.

## Verificação

### Simular a Falha do Link

```cisco
enable
configure terminal
interface ethernet 0/1
shutdown
```

### Verificar Rotas no R1

```cisco
show ip route
```

### Testar Traceroute do PC1

```cisco
trace 192.168.10.1
trace 192.168.20.2
```

## Conclusão

A resposta correta depende das rotas configuradas em sua topologia específica. O objetivo deste lab é desenvolver a capacidade de **raciocinar sobre o encaminhamento de pacotes** antes de executar os comandos, treinando a análise da tabela de roteamento e a compreensão de next-hop reachability.
