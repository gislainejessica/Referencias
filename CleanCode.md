## Boas praticas (Código React, React-Native, Javascript)

- Desestruturar os props (Para que fica mais facil enteder quaisatributos aquele componete está usando) 
*Quais props estão atrelados a determinado componente*
- Colocar componets em arquivos separados (Por funcionalidades)
- Usando padrão de nomeamento de variáveis 
- Fugir da armadilha do boolean (Ex.: Estilização => Hieranquia)
- Usar fat-arrow-functions `() => {}` Simplifica 
- Colocar funções independentes fora de Hooks customizados
- Se mantenha consistente 
`imports ;
exports ;
nomeação de componentes ; 
hooks ;
nome de classes ; 
HOC'S `
- Componetizar componentes duplicados (Se codigo se repete em varias parte, torna-lo um componente reutilizavel)
- Mater os componentes simples (Evitar fazer o componentes ficarem desnecessariamente complicados) 
(não colocar multiplas funções a um só componente) `=>` facilita os testes unitários
- **useReducer** se **useState** se tornar complexo demais para o problema
- Usar declaração de funções em areas sem brilho, onde outros podem precisar entender melhor a função de determinadada 
parte do código
-Usar Prettier para pre-configurar a estilização do código
- Usar `<> </>` em vez de `<Fragment><Fragment>`
- Colocar as coisas em ordem
* Variaveis em ordem (alfa)
* Funções em oredem (alfa, funcional)
` 1 React import 
2 Bibliotecas import (alfa) 
3 Absolute Maiusculo file projeto import (alfa) 
4 Relative Minusculo file import (alfa) 
5 import * as
6 import '<algum arquivo>.<extensão>'`

