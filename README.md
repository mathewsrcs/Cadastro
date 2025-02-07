# Cadastro de Usuários

Este é um sistema de **cadastro de usuários** desenvolvido em **C#** que permite adicionar, buscar e excluir usuários, armazenando os dados em um arquivo de texto.

## 🚀 Funcionalidades

- 📌 **Cadastrar um novo usuário**
- 🔍 **Buscar um usuário pelo documento**
- 🗑️ **Excluir um usuário pelo documento**
- 💾 **Armazenar e carregar dados de um arquivo**

## 🛠️ Tecnologias Utilizadas

- **C#**
- **.NET Console Application**
- **Manipulação de arquivos**

## 📂 Estrutura do Projeto

```
/cadastroUsers
│-- Program.cs
│-- baseDeDados.txt (gerado automaticamente)
│-- README.md
```

## 🏗️ Estruturas Principais

### **1. Estruturas de Dados**

#### `DadosCadastraisStruct`

Define as informações do usuário:

```csharp
public struct DadosCadastraisStruct
{
    public string Nome;
    public DateTime DataDeNascimento;
    public string NomeDaRua;
    public UInt32 NumeroDaCasa;
    public string NumeroDoDocumento;
}
```

#### `Resultado_e`

Define os estados do programa:

```csharp
public enum Resultado_e
{
    Sucesso = 0,
    Sair = 1,
    Excecao = 2
}
```

### **2. Principais Métodos**

- `CadastraUsuario()` → Captura os dados do usuário e os salva na lista.
- `BuscaUsuarioPeloDoc()` → Busca usuários pelo número do documento.
- `ExcluiUsuarioPeloDoc()` → Exclui usuários pelo número do documento.
- `GravaDados()` → Salva os dados no arquivo `baseDeDados.txt`.
- `CarregaDados()` → Carrega os dados do arquivo para a memória.

## 🎮 Como Executar

1. **Clone o repositório**
   ```sh
   git clone https://github.com/seu-usuario/cadastroUsers.git
   ```
2. **Abra o projeto no Visual Studio**
3. **Compile e execute o programa**
4. **Utilize as opções do menu**




