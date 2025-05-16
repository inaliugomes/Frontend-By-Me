# ⚛️REACT HOOKS

## ✅ UseState

O useState é um hook que permite ao React armazenar valores no estado de um componente funcional . 

Sempre que esse valor é alterado, o React atualiza o estado e renderiza o componente com o **Novo valor**

```js
const [contador, setContador] = useState(0);

```
Ou seja quando a variavél **contador** for alterado o **UseSate** será chamadado e o componente será renderizado na tela. 


## 🕒 Quando usar o UseEffective

Devemos usar o **useEffect** quando precisamos:

- Trabalhar con  funções assíncronas(como **fetch**, **azios**, etc)

- Buscar dados de uma **API ou endpint externo**

- Monitor variáveis (como props ou estados) e executar ações sempre que elas mudarem . 

- Excecutar uma ação na **montagem ou desmontagem do componente**

```js
useEffect(() => {
  // Código que será executado
}, [dependencias]);

//()=>{}: função que será executada.

//[]: lista de dependências (variáveis que, ao mudarem, fazem o efeito rodar de novo).

//Se o array estiver vazio, o efeito só roda uma vez, na montagem do componente.

```

## ✅ Batching 

Batching é  um processo em que o React **Agrupa múltiplas atualizações de estados (useState)** que ocorrem juntas, para evitar renderizações desnecessárias. 
Ou seja, o React só renderiza o componente **Uma vez no final**, mesmo que vários estados seja atualizados ao mesmo tempo. 