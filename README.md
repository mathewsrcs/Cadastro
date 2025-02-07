# Cadastro de Usuários

## Este é um projeto de cadastro de usuários que permite adicionar, editar, visualizar e excluir informações de usuários.
```
Tecnologias Utilizadas:
```
C#

```
Funcionalidades
```
Cadastro de novos usuários

Listagem de usuários cadastrados

Exclusão de usuários

# Explicação do Código
```
1. Estruturas e Enumerações
```
struct DadosCadastraisStruct
Define os dados cadastrais de um usuário:

Nome (string)
DataDeNascimento (DateTime)
NomeDaRua (string)
NumeroDaCasa (UInt32)
NumeroDoDocumento (string)
enum Resultado_e
Define os possíveis retornos das funções:

Sucesso (0)
Sair (1)
Excecao (2)
```
2. Funções Auxiliares
```
MostraMensagem(string mensagem)

Exibe uma mensagem no console e aguarda que o usuário pressione uma tecla para continuar.
PegaString(ref string minhaString, string mensagem)

Solicita uma entrada do usuário e a armazena na variável referenciada. Se o usuário digitar "S", retorna Sair.
PegaData(ref DateTime data, string mensagem)

Solicita uma data e verifica se o formato é válido. Caso contrário, solicita novamente.
PegaUInt32(ref UInt32 numeroUInt32, string mensagem)

Solicita um número inteiro positivo e garante que seja válido.
```
3. Cadastro de Usuários
```
CadastraUsuario(ref List<DadosCadastraisStruct> ListaDeUsuarios)

Solicita os dados do usuário via console e os armazena em uma lista.
Grava os dados no arquivo baseDeDados.txt.
GravaDados(string caminho, List<DadosCadastraisStruct> ListaDeUsuarios)

Salva a lista de usuários no arquivo de texto.
```
4. Carregamento e Manipulação de Dados
```
CarregaDados(string caminho, ref List<DadosCadastraisStruct> ListaDeUsuarios)

Lê os dados do arquivo e carrega na lista de usuários.
BuscaUsuarioPeloDoc(List<DadosCadastraisStruct> ListaDeUsuarios)

Busca um usuário pelo número do documento e exibe seus dados.
ExcluiUsuarioPeloDoc(ref List<DadosCadastraisStruct> ListaDeUsuarios)

Remove um usuário da lista com base no número do documento e atualiza o arquivo.
```
5. Método Principal Main
```
Inicializa variáveis e define as tags que serão usadas no arquivo de texto.
Carrega os dados do arquivo baseDeDados.txt.
Exibe um menu interativo com as opções:
"C" para cadastrar um usuário.
"B" para buscar um usuário.
"E" para excluir um usuário.
"S" para sair do programa.
Processa a entrada do usuário e executa a ação correspondente.
O loop continua até que o usuário escolha sair ("S").
Fluxo Geral do Programa
Inicia o programa e carrega os usuários já cadastrados.
Exibe o menu de opções.
O usuário pode:
Cadastrar um novo usuário (solicita dados e os salva).
Buscar um usuário pelo documento (mostra os dados).
Excluir um usuário pelo documento (remove da lista e do arquivo).
Sair do programa.
```
Resumo
```
✔ Usa struct para representar usuários.
✔ Lê e grava dados em um arquivo de texto.
✔ Possui tratamento de erros para entrada inválida.
✔ Usa enum para definir estados do programa.
✔ Usa listas para armazenar múltiplos usuários.

Esse código é um sistema básico de CRUD (Create, Read, Update, Delete) para gerenciamento de usuários. 🚀
