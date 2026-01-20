## Resumo 
### Tipos de arquitetura:
- Software - mais próximo ao código, fazer com que o software dure mais tempo
- Solução - ajuda a desenhar a solução pra entregar mais valor, mais próximo ao cliente, entender a solução como um todo
- Tecnológica - vem de tecnologias específicas (ferramentas especializadas)
- Corporativa - como a empresa funciona como um todo (pessoas, processos, tecnologia, governança)

### Arquitetura de software
* Diretamente ligada ao processo de desenvolvimento
* Afeta diretamente a estrutura organizacional da empresa
    * formação dos times
    * estrutura dos componentes do software

Papel do arquiteto de software:
- Transformar requisitos de negócio em padrões de arquitetura
- Orquestrar pessoas desenvolvedoras e experts de domínio
- Entender de forma profunda conceitos e modelos arquiteturais
- Auxilia na tomada de decisao nos momentos de crise
- Reforca boas praticas de desenvolvimento

Diferenca entre arquitetura e design de software:
| Arquitetura de Software | Design de Software |
| ---------------------- | ------------------ |
| Escopo global ou alto nivel | Escopo local |


Estruturas - Coisas que tenho que pensar quando arquitetando um software:

Componente-conector:
![alt text](./img/03/componente-conector.png)
Exemplo: todas "bolinhas" apresentadas no desenho sao formas de conectar
- Iteracao entre elementos para garantir o funcionamento do sistema
- Componentes -> comportamento do sistema
    * Services, clients, servers, pipelines
- Iteracoes -> conectores (iteracoes entre os componentes)
    * Como os conectores se comunicam (protocolos, APIs, eventos)

Módulos
- Unidade de software
- Pacotes
- Responsabilidades funcionais
- Camadas
- Visão mais micro

Estrutura de Alocação:
- E a relacao das estruturas componente-conector e módulos e como elas se conectam com "não software"
    * Tipo de computacao (tipo de maquina)
    * Ambientes (onde vou testar)
    * Testes
    * Build
    * Deployment


### Efeito "Ivory tower" ou torre de marfim
Quando o arquiteto se isola do dia-a-dia do time de desenvolvimento, se torna um especialista teórico que pensa estar resolvendo problemas, mas esta completamente desconectado da realidade do time e do produto.

## Decisões arquiteturais
Decisões "erradas" para iniciar o desenvolvimento de software:
- Problemas de waterfall - muita especificação sem geração de código
- Arquitetura de CRUD 
- Começar pelas ferramentas
- Começar sem testes
- Começar sem processos de CI (continous integration)

Por onde começar:

![middle-out](./img/03/middle-out.png)

Middle-out: foco em começar o desenvolvimento pelos componentes core e mais críticos do sistema.
Maior flexibilidade, ou seja, menor complexidade para integração com outros sistemas e começar pelo meio permite mais mudanças, desenvolvimento incremental e facilidade na escala.

## Dimensões e fitness functions

Arquitetura multidimensional:

* Técnica: Tecnologia, frameworks, acoplamento, testes, performance.

* Dados: Como dados irão trafegar, qual formato, como vai acontecer a sincronização dos dados...

* Segurança: rate limit, evitar man in the middle, mTLS, formato de log...

* Operacional: Como vai operar, observabilidade, pipelines, testes, rollback...

