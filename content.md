# Desvendendo o Context API

### O que é Context API
O **Context API** no React é uma biblioteca que permite compartilhar dados entre componentes sem a necessidade de passá-los explicitamente através das props. É como ter uma mochila   onde você guarda informações importantes e qualquer componente pode pegar o que precisa.

```
  // Criando um contexto
  export const AuthContext = createContext();

  // Criando o provider
  function AuthProvider({ children }){
    return(
      <AuthContext.Provider value={{ informacaoImportante }}>
        {children}
      </AuthContext.Provider>
    )
  }
  export default AuthProvider;


  // Use provider para envolver os componentes que querem acessar o contexto
  <AuthProvider>
    <RouterProvider router={router} />
  </AuthProvider>
```

### Exemplos com Código de Context API
No exemplo acima, criamos um contexto chamado **AuthContext**. O componente(**children**) envolto em <AuthContext.Provider> terá acesso à informação (**informacaoImportante**) que pode ser consumida por qualquer componente dentro dele usando <AuthProvider>.


# Desvendando o Redux

### O que é Redux
O **Redux** é um gerenciador de estado para aplicações JavaScript, especialmente útil em projetos complexos. Ele age como um segurança para o estado da sua aplicação, mantendo a ordem e facilitando o acesso a informações cruciais.

```
  // Criando uma ação
  const aumentarContador = () => {
    return {
      type: 'AUMENTAR_CONTADOR'
    };
  };

  // Criando o reducer
  const contador = (estado = 0, acao) => {
    switch (acao.type) {
      case 'AUMENTAR_CONTADOR':
        return estado + 1;
      default:
        return estado;
    }
  };

  // Configurando Redux store
  const { createStore } = Redux;
  const store = createStore(contador);
```

### Exemplos com Código de Redux
Neste exemplo, definimos uma ação(aumentarContador) e o reducer(contador). O Redux (store) gerencia o estado da aplicação, e a ação AUMENTAR_CONTADOR incrementa o contador.


# Context API vs. Redux: Escolhendo sua Arma

## Explique a Diferença entre Context API e Redux
A **Context API** é mais como um rádio walkie-talkie, conectando componentes diretamente para compartilhar pequenas informações. Enquanto isso, o Redux age como uma central de comando, ideal para aplicações maiores que requerem uma gestão mais robusta de estado.

## Quando Usar Context API ou Redux?
Se sua aplicação é uma pequena reunião de amigos, vá de **Context API**. Se está organizando uma conferência global com milhares de participantes, escolha Redux para manter tudo sob controle. Em resumo, Context API para o simples, Redux para o grandioso.

## Conclusão
Curtiu esse conteúdo? me siga no [Linkedin](https://www.linkedin.com/in/daniel-felix-developer/)

**Fontes de produção**
Ilustrações da capa: Imagem retirada do site www.toptotal.com e modificada com Power Point
Conteúdo gerado por: ChatGPT e revisões humana

# Link do artigo publicado na plataforma da Digital Innovation One
[Artigo](https://web.dio.me/articles/redux-ou-context-api-decifrando-as-opcoes-de-gerenciamento-de-estado-no-react?back=%2Farticles&page=1&order=oldest)