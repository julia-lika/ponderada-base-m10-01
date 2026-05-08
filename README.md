# Aplicativo Nativo em Kotlin — Atividade de Sala

## Desenvolvimento da aplicação

Durante o desenvolvimento do aplicativo, alguns ajustes e melhorias foram realizados:

- Inicialmente, houve problemas relacionados às dependências do Gradle, principalmente envolvendo compatibilidade de versões entre o AGP (Android Gradle Plugin) e o AndroidX.

- Após a correção das dependências, foi identificado um erro na lógica de geração aleatória do dado: os valores estavam sendo exibidos de `0` a `5`. O problema foi resolvido adicionando `+1` ao resultado do `Random.nextInt()`.

- Foram adicionados novos tipos de dados à aplicação, incluindo:
  - D10
  - D20
  - D100

- Os novos dados foram inseridos dentro de uma lista chamada `dados`, permitindo que os botões de seleção fossem gerados dinamicamente na interface utilizando `forEach`.

```kotlin
val dados = listOf("D6", "D10", "D20", "D100")
```

* Também foram inseridas imagens representando visualmente cada tipo de dado. As imagens foram adicionadas na pasta `drawable` do projeto e exibidas dinamicamente utilizando uma estrutura `when`, que altera a imagem de acordo com o dado selecionado.

```kotlin
val imagemDado = when (dadoSelecionado) {
    "D6" -> R.drawable.d6
    "D10" -> R.drawable.d10
    "D20" -> R.drawable.d20
    "D100" -> R.drawable.d100
    else -> R.drawable.d6
}
```

<video width="600" controls>
  <source src="video.mp4" type="video/mp4">
</video>

[![Assistir vídeo]](./video.mp4)