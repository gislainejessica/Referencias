## Uso de React Hooks conceitos a serem observados

- **useState**: É uma alternativa para mantermos nosso estado quando o mesmo é mais complexo. Então quando precisamos utilizar estados dentro dos componentes, ou seja, precisamos de variaveis onde podemos guardar e mudar o estado da mesma quando necessário estando disponível para todo componente quando requisitado). Nesse caso devemos usar **_useState_** para criar a variar e a função que ira setar essa variavel quando necessário. Por convenção usamos o prefixo **_set_** antes da variavel que representa a função para mudar o estado.
```js
  const [variavel setVariavel] = useState()
``` 

- **useEffect**: Ajudar a lidar com **side effects**. O primeiro parâmetro do useEffect é uma função de callback que irá ser disparada quando o componente for montado. Basicamente usamos useEfeect quando precisamos fazer uma requisição a api externa, fazer alguma função rodar dada mudanças em alguma variavel
```js
  useEffect(() => {
    if (variavelVigiada === "atualizei"){
       console.log('Tô trabalhando aqui.')
    }
  },[variavelVigiada])

```
  
- **useMemo**:
- **useCallback**:


- **useContext**:
- **useReducer**:
- **useRef**:

- **useImperativeHandle**: 
- **useLayoutEffect**:
- **useDebugValue**:

