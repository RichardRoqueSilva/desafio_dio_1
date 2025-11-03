# MeuPrimeiroAppDIO

Este é um projeto de demonstração criado para um desafio de desenvolvimento mobile, focado em implementar conceitos básicos de **Jetpack Compose** e **Internacionalização (i18n)** em um aplicativo Android.

## Funcionalidades Implementadas

1.  **UI em Jetpack Compose:** A interface do usuário é construída usando a biblioteca Compose.
2.  **Internacionalização (i18n):** O aplicativo suporta múltiplos idiomas (Português, Inglês, Espanhol) para a mensagem principal.
3.  **Centralização de Conteúdo:** A mensagem principal é exibida perfeitamente centralizada na tela usando um `Box` com `Alignment.Center`.

## Estrutura do Projeto

O código principal se encontra em `MainActivity.kt` e a lógica de internacionalização reside nos arquivos `strings.xml` localizados em `res/values/`.

### 1. Internacionalização (i18n)

Para suportar múltiplos idiomas, foram criados os seguintes arquivos de recursos:

| Idioma | Código | Diretório | Exemplo de String Central (`saudacao_inicial`) |
| :--- | :--- | :--- | :--- |
| Português (Padrão) | `pt` (ou padrão) | `res/values/strings.xml` | `Esse é o primeiro aplicativo do %1$s!` |
| Inglês | `en` | `res/values-en/strings.xml` | `This is %1$s's first app!` |
| Espanhol | `es` | `res/values-es/strings.xml` | `¡Esta es la primera aplicación de %1$s!` |

**Nota sobre Placeholders:** Foi utilizado o formato `%1$s` nas strings para indicar onde o nome do usuário (o parâmetro passado) deve ser inserido dinamicamente pelo `stringResource()`.

### 2. Centralização na Tela

O componente `Greeting` é centralizado usando um `Box` dentro do `Scaffold`:

*   O `Scaffold` gerencia o espaço da barra de status/navegação (através de `innerPadding`).
*   Um `Box` recebe este `innerPadding` e usa o modificador `contentAlignment = Alignment.Center` para posicionar seu conteúdo (o `Text`) no centro exato da tela.
