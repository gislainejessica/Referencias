## Boas praticas (Código React, React-Native, Javascript)

- Desestruturar os props: para se enteder melhor quais atributos aquele componente está usando, ou seja, quais props estão                    atrelados a determinado componente.
  
- Colocar componentes em arquivos separados (separados por funcionalidades).
- Usar padrão de nomeamento de variáveis. 
- Fugir da armadilha do boolean (Ex.: Estilização => Hieranquia).
- Usar fat-arrow-functions: `() => {}` Simplifica o código.
- Colocar funções independentes fora de Hooks customizados, para não carregar o hooks com funcionalidades que não são estritamente inerentes a eles.
- Se mantenha consistente em: 

  ```
  imports 
  exports 
  nomeação de componentes  
  hooks 
  nome de classes  
  HOC'S
  
- Componentizar códigos duplicados: se o código se repete em várias partes, torná-lo um componente reutilizável
- Mater o componente simples: evitar fazer componentes desnecessariamente complicados.
  Exemplo: Não colocar multiplas funções em um só componente`=>` isso facilitará os testes unitários.
  
- Usar o **useReducer** se **useState** se tornar complexo demais para o problema.
- Usar declaração de funções em areas sem brilho: locais onde pode-se precisar entender melhor uma função que pode ser usada externamente, por exemplo. Ex:`Function nomeFacildeEnteder(){}`

- Usar Prettier para pré-configurar a estilização do código: facilita padronização e trabalho em equipe.
- Usar `<> </>` em vez de `<Fragment><Fragment>`
- Colocar as coisas em ordem
  * Variaveis em ordem (alfa)
  * Funções em ordem (alfa, funcional)
    ``` 
    1 React import 
    2 Bibliotecas import (alfa) 
    3 Absolute Maiusculo file projeto import (alfa) 
    4 Relative Minusculo file import (alfa) 
    5 import * as
    6 import '<algum arquivo>.<extensão>'`

