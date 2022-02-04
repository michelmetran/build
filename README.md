## Build

<br>

Instalar o build

```bash
python3 -m pip install build
python3 -m pip install --upgrade build
```

<br>

Builda o package localmente

```bash
python3 -m build
```

<br>

Instala o *build* localmente

```
!pip install dist/traquitanas*.tar.gz  
```

https://packaging.python.org/tutorials/packaging-projects/

<br>

## Git Actions: publicar pacotes no PyPi

<br>

Publicar versões de distribuição de pacotes usando fluxos de trabalho de CI / CD de ações do GitHub. Ver mais [aqui](https://packaging.python.org/guides/publishing-package-distribution-releases-using-github-actions-ci-cd-workflows/).

**IMPORTANTE**: Adicionar as credenciais do PyPi, da versão test e versão estável, como um Secrets do GitHub, sob os nomes PYPI_API_TOKEN e TEST_PYPI_API_TOKEN.

<br>

----

## *Tags*

Note que a função tem uma condição: o pacote só é publicado quando há uma tag de versão no *commit*. Isso condicionante pode ser suprimida ou empregada. É preciso entender os conceitos de [tags](https://git-scm.com/book/en/v2/Git-Basics-Tagging) em *commits* e como fazer isso usando o [PyCharm](https://www.jetbrains.com/help/pycharm/use-tags-to-mark-specific-commits.html#tag_commit) ou outra IDE

<br>

----

## Arquivos

### setup.cfg

[**SetupTools**: Configuring setup() using setup.cfg files](https://setuptools.readthedocs.io/en/latest/userguide/declarative_config.html)

<br>

### pyproject.toml

Pelo que li e entendi, é necessário esse arquivo quando não existe arquivo setup.py.

[**SetupTools**: setup.cfg-only projects](
https://setuptools.readthedocs.io/en/latest/setuptools.html#setup-cfg-only-projects)

<br>

### MANIFEST.in

O arquivo MANIFEST.in define quais arquivos precisam estar no *build*. Para maiores informações [clicar aqui](https://packaging.python.org/guides/using-manifest-in/)

<br>

### .editorconfig

Meu amigo tunisiano sugeriu eu acrescentar um arquivo ```.editorconfig``` na raiz do meu projeto. O conteúdo do arquivo era como apresentado abaixo:

```bash
# EditorConfig is awesome: https://EditorConfig.org
root = true

[*]
charset = utf-8
indent_size = 2
indent_style = space
insert_final_newline = true
trim_trailing_whitespace = true
end_of_line = crlf

[*.py]
indent_size = 4
max_line_length = 119

```

<br>

Num primeiro momento, achei que o arquivo era imprescindível e depois, lendo, descobri que não, porém é adotado como boa prática, visando manter a configuração.

<br>

**Referências**

- [Why You Should Use EditorConfig to Standardize Code Styles](https://www.freecodecamp.org/news/how-to-use-editorconfig-to-standardize-code-styles/)
- [EditorConfig](https://editorconfig.org/)

<br>

## Estudar

<br>

### Version

<br>

Add version in traquitanas.__version__

- [**StackOverflow**: Creating a  __version __ attribute for python packages without getting into trouble](https://stackoverflow.com/questions/17791481/creating-a-version-attribute-for-python-packages-without-getting-into-troubl)
