# 🛒 Lista de Compras

<div align="center">

# 🛍️ Aplicativo Lista de Compras

### Projeto Mobile desenvolvido com React Native, Expo e TypeScript

<br>

![React Native](https://img.shields.io/badge/React%20Native-blue?style=for-the-badge&logo=react)
![Expo](https://img.shields.io/badge/Expo-black?style=for-the-badge&logo=expo)
![TypeScript](https://img.shields.io/badge/TypeScript-blue?style=for-the-badge&logo=typescript)

<br>

**Projeto desenvolvido como atividade prática de desenvolvimento de aplicações mobile.**

</div>

---

## 📱 Sobre o projeto

O **Lista de Compras** é uma aplicação mobile criada utilizando **React Native**, **Expo** e **TypeScript**.

A atividade teve como objetivo desenvolver um aplicativo simples e funcional, colocando em prática conceitos importantes de programação mobile e organização de projetos.

Com o aplicativo, o usuário pode:

- 📝 Cadastrar produtos;
- ➕ Adicionar novos itens à lista;
- 🔢 Definir a quantidade de cada produto;
- ❌ Excluir itens;
- ⚠️ Receber avisos quando informações obrigatórias não forem preenchidas;
- 📊 Acompanhar a quantidade de itens cadastrados;
- 🧺 Visualizar uma mensagem quando a lista estiver vazia;
- 📱 Executar o projeto diretamente no celular através do Expo Go.

---

## 🎯 Objetivo

O objetivo principal desta atividade foi praticar a criação de uma aplicação utilizando **React Native com TypeScript**.

Durante o desenvolvimento foram trabalhados conceitos como:

- Componentização;
- `useState`;
- TypeScript;
- Props;
- Formulários;
- Validação;
- `FlatList`;
- Eventos de interação;
- Organização dos arquivos;
- Estrutura de um projeto Expo.

A aplicação também foi dividida em componentes para deixar o código mais organizado e facilitar sua manutenção.

---

## 🚀 Tecnologias

| Tecnologia | Função |
|---|---|
| ⚛️ React Native | Criação da interface do aplicativo |
| 📦 Expo | Execução e gerenciamento do projeto |
| 🔷 TypeScript | Tipagem e segurança do código |
| 📱 Expo Go | Testes do aplicativo no celular |
| 📋 FlatList | Renderização dos produtos |
| 🧩 Componentes | Organização da aplicação |

---

## 📂 Organização dos arquivos

```text
lista-de-compras/
│
├── components/
│   ├── Cabecalho.tsx
│   ├── FormularioItem.tsx
│   ├── ItemCompra.tsx
│   └── ListaCompras.tsx
│
├── App.tsx
├── index.tsx
├── types.ts
├── package.json
├── app.json
├── babel.config.js
└── tsconfig.json
```

A aplicação foi organizada em componentes independentes, deixando cada parte do aplicativo responsável por uma função específica.

---

## 🧩 Componentes utilizados

### 🏷️ Cabecalho

O componente `Cabecalho.tsx` apresenta a identificação principal da aplicação.

```text
🛒 Minha Lista de Compras

Organize suas compras de forma simples
```

---

### 📝 FormularioItem

O `FormularioItem.tsx` permite cadastrar um novo produto.

O usuário pode informar:

- Nome do produto;
- Quantidade;
- E utilizar o botão **Adicionar item**.

Também existe uma validação para impedir que um produto seja cadastrado sem nome.

---

### 🛍️ ItemCompra

O componente `ItemCompra.tsx` representa cada produto apresentado na lista.

Cada item mostra:

```text
Nome do produto
Qtd: quantidade
```

Além disso, possui um botão `✕` que permite remover o produto.

---

### 📋 ListaCompras

O componente `ListaCompras.tsx` apresenta todos os produtos cadastrados utilizando o `FlatList`.

Quando não existem produtos, o aplicativo apresenta:

```text
🧺

Sua lista está vazia

Adicione um produto no campo acima
```

---

## 🔷 Tipagem com TypeScript

Para organizar os dados dos produtos, foi criada a interface:

```typescript
export interface ItemDeCompra {
  id: string;
  nome: string;
  quantidade: number;
}
```

Dessa forma, cada item possui uma estrutura definida e o código fica mais organizado.

---

## ⚛️ Gerenciamento dos itens

O aplicativo utiliza o `useState` para armazenar e atualizar os produtos da lista.

Exemplo:

```tsx
const [itens, setItens] = useState<ItemDeCompra[]>([]);
```

Quando um produto é adicionado, o estado é atualizado.

Quando um produto é excluído, ele é retirado da lista e a tela é atualizada automaticamente.

---

## 🔄 Funcionamento do aplicativo

O fluxo principal da aplicação pode ser representado assim:

```text
                 🛒
          Lista de Compras
                 │
                 ▼
          📝 Novo produto
                 │
                 ▼
        Nome + Quantidade
                 │
                 ▼
          ➕ Adicionar item
                 │
                 ▼
            📋 Produtos
             │       │
             │       │
             ▼       ▼
          🛍️ Item   ❌ Excluir
             │
             ▼
       Lista atualizada
```

---

## 🧪 Testes realizados

Foram realizados diferentes testes para confirmar o funcionamento do aplicativo.

### ✅ Adicionar produto

Foi verificado se um novo produto é incluído corretamente na lista.

### ✅ Validação do nome

Foi testado o cadastro sem informar o nome do produto.

Nesse caso, o aplicativo apresenta um alerta solicitando o preenchimento.

### ✅ Quantidade padrão

Quando a quantidade não é informada, o aplicativo utiliza:

```text
1
```

como quantidade padrão.

### ✅ Remover produto

Foi testada a exclusão de produtos através do botão `✕`.

### ✅ Lista vazia

Depois da remoção de todos os produtos, é apresentada a mensagem informando que a lista está vazia.

### ✅ Contador

Também foi verificado se o contador de produtos é atualizado conforme os itens são adicionados ou removidos.

---

## ▶️ Como executar

### 1. Instalar as dependências

No terminal do projeto:

```bash
npm install
```

### 2. Iniciar o Expo

```bash
npx expo start
```

### 3. Abrir no celular

Com o **Expo Go** instalado:

1. Conecte o celular e o computador à mesma rede Wi-Fi;
2. Execute `npx expo start`;
3. Aguarde o QR Code aparecer;
4. Abra o Expo Go;
5. Escaneie o QR Code;
6. Aguarde o aplicativo carregar.

---

## 🔍 Verificando o TypeScript

Para verificar possíveis erros de tipagem:

```bash
npx tsc --noEmit
```

Se não aparecer nenhuma mensagem de erro, o TypeScript foi verificado com sucesso.

---

## 📚 Conhecimentos praticados

Durante o desenvolvimento desta atividade foram praticados:

- ⚛️ React Native;
- 🔷 TypeScript;
- 🧠 `useState`;
- 📦 Props;
- 📝 Formulários;
- ⚠️ Validação de informações;
- 📋 `FlatList`;
- 👆 `TouchableOpacity`;
- 🚨 `Alert`;
- 📱 `SafeAreaView`;
- 🗂️ Organização de componentes;
- 🔄 Atualização de estado.

---

## 💡 Aprendizado

A atividade possibilitou colocar em prática a criação de uma aplicação mobile utilizando React Native e Expo.

Também foi possível compreender melhor como organizar uma aplicação através de componentes, trabalhar com estados, receber informações através de props e utilizar TypeScript para definir os tipos dos dados.

---

## 👩‍💻 Desenvolvedora

<div align="center">

# Quezia da Paz Brito Silva

🎓 **Estudante de Desenvolvimento de Sistemas**

<br>

💻 Desenvolvimento Mobile  
⚛️ React Native  
📦 Expo  
🔷 TypeScript

</div>

---

<div align="center">

### 🛒 Lista de Compras

**Projeto desenvolvido para praticar conceitos de desenvolvimento mobile.**

✨ Feito com dedicação e aprendizado.

</div>
