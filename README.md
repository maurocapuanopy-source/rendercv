<div align="center">
<h1>RenderCV</h1>

_Gerador de currículos para acadêmicos e engenheiros, disponível em [rendercv.com](https://rendercv.com)_

[![test](https://github.com/rendercv/rendercv/actions/workflows/test.yaml/badge.svg?branch=main)](https://github.com/rendercv/rendercv/actions/workflows/test.yaml)
[![coverage](https://coverage-badge.samuelcolvin.workers.dev/rendercv/rendercv.svg)](https://coverage-badge.samuelcolvin.workers.dev/redirect/rendercv/rendercv)
[![docs](<https://img.shields.io/badge/docs-mkdocs-rgb(0%2C79%2C144)>)](https://docs.rendercv.com)
[![pypi-version](<https://img.shields.io/pypi/v/rendercv?label=PyPI%20version&color=rgb(0%2C79%2C144)>)](https://pypi.python.org/pypi/rendercv)
[![pypi-downloads](<https://img.shields.io/pepy/dt/rendercv?label=PyPI%20downloads&color=rgb(0%2C%2079%2C%20144)>)](https://pypistats.org/packages/rendercv)

</div>

Escreva seu CV ou currículo em YAML e execute o RenderCV,

```bash
rendercv render John_Doe_CV.yaml
```

e obtenha um PDF com tipografia perfeita.

Com o RenderCV, você pode:

- Controlar a versão do seu currículo — é apenas texto.
- Focar no conteúdo — não se preocupe com a formatação.
- Obter tipografia perfeita — alinhamento e espaçamento consistentes, tudo resolvido para você.

Um arquivo YAML como este:

```yaml
cv:
  name: John Doe
  location: San Francisco, CA
  email: john.doe@email.com
  website: https://rendercv.com/
  social_networks:
    - network: LinkedIn
      username: rendercv
    - network: GitHub
      username: rendercv
  sections:
    Bem-vindo ao RenderCV:
      - O RenderCV lê um currículo escrito em um arquivo YAML e gera um PDF com tipografia profissional.
      - Consulte a [documentação](https://docs.rendercv.com) para mais detalhes.
    educação:
      - institution: Princeton University
        area: Computer Science
        degree: PhD
        date:
        start_date: 2018-09
        end_date: 2023-05
        location: Princeton, NJ
        summary:
        highlights:
          - "Tese: Busca Eficiente de Arquitetura Neural para Implantação com Restrição de Recursos"
          - "Orientador: Prof. Sanjeev Arora"
          - Bolsa de Pesquisa de Pós-Graduação da NSF, Siebel Scholar (Turma de 2022)
    ...
```

torna-se um destes PDFs. Clique nas imagens para visualizar.

| [![Exemplo do Tema Classic do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/classic.png)](https://github.com/rendercv/rendercv/blob/main/examples/John_Doe_ClassicTheme_CV.pdf)    | [![Exemplo do Tema Engineeringresumes do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/engineeringresumes.png)](https://github.com/rendercv/rendercv/blob/main/examples/John_Doe_EngineeringresumesTheme_CV.pdf) | [![Exemplo do Tema Sb2nov do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/sb2nov.png)](https://github.com/rendercv/rendercv/blob/main/examples/John_Doe_Sb2novTheme_CV.pdf) |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [![Exemplo do Tema Moderncv do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/moderncv.png)](https://github.com/rendercv/rendercv/blob/main/examples/John_Doe_ModerncvTheme_CV.pdf) | [![Exemplo do Tema Engineeringclassic do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/engineeringclassic.png)](https://github.com/rendercv/rendercv/blob/main/examples/John_Doe_EngineeringclassicTheme_CV.pdf) | ![Temas personalizados podem ser adicionados.](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/customtheme.png)                                                                                        |


## JSON Schema

O JSON Schema do RenderCV permite preencher o YAML interativamente, com preenchimento automático e documentação em linha.

![JSON Schema do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/json_schema.gif)


## Extensas Opções de Design

Você tem controle total sobre cada detalhe.

```yaml
design:
  theme: classic
  page:
    size: us-letter
    top_margin: 0.7in
    bottom_margin: 0.7in
    left_margin: 0.7in
    right_margin: 0.7in
    show_footer: true
    show_top_note: true
  colors:
    body: rgb(0, 0, 0)
    name: rgb(0, 79, 144)
    headline: rgb(0, 79, 144)
    connections: rgb(0, 79, 144)
    section_titles: rgb(0, 79, 144)
    links: rgb(0, 79, 144)
    footer: rgb(128, 128, 128)
    top_note: rgb(128, 128, 128)
  typography:
    line_spacing: 0.6em
    alignment: justified
    date_and_location_column_alignment: right
    font_family: Source Sans 3
  # ...e muito mais
```

![Opções de Design do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/design_options.gif)

> [!TIP]
> Deseja configurar um ambiente de visualização ao vivo como o mostrado acima? Veja [como configurar o VS Code para o RenderCV](https://docs.rendercv.com/user_guide/how_to/set_up_vs_code_for_rendercv).

## Validação Estrita

Sem surpresas. Se algo estiver errado, você saberá exatamente o que e onde. Se for válido, você recebe um PDF perfeito.

![Recurso de Validação Estrita do RenderCV](https://raw.githubusercontent.com/rendercv/rendercv/main/docs/assets/images/validation.gif)


## Qualquer Idioma

Preencha o campo locale para o seu idioma.

```yaml
locale:
  language: portuguese
  last_updated: Última atualização em
  month: mês
  months: meses
  year: ano
  years: anos
  present: presente
  month_abbreviations:
    - Jan
    - Fev
    - Mar
  ...
```

## Começando

Instale o RenderCV (Requer Python 3.12+):

```
pip install "rendercv[full]"
```

Crie um novo arquivo yaml de currículo:

```
rendercv new "John Doe"
```

Edite o YAML e depois renderize:

```
rendercv render "John_Doe_CV.yaml"
```

Para mais detalhes, consulte o [guia do usuário](https://docs.rendercv.com/user_guide/).
