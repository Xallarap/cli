---



copyright:

  years: 2015, 2018
lastupdated: "2018-08-09"

---

{:codeblock: .codeblock}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}


# Instalando a CLI  {{site.data.keyword.Bluemix_notm}}  Independente
{: #install_use}

O {{site.data.keyword.Bluemix_notm}} CLI fornece a interface da linha de comandos para gerenciar aplicativos, contêineres, infraestruturas, serviços e outros recursos no {{site.data.keyword.Bluemix_notm}}.

Se você desejar instalar a CLI do {{site.data.keyword.Bluemix}} e outros plug-ins e ferramentas recomendadas para
desenvolver aplicativos para o {{site.data.keyword.Bluemix_notm}}, siga o método descrito
[aqui](/docs/cli/index.html).
{: tip}

Use as etapas a seguir para instalar a CLI do {{site.data.keyword.Bluemix_notm}} independente:

1. Selecione o instalador do OS para download

   Mac OS X de 64 bits:
[instalador](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx){: new_window} /
[sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/checksum){: new_window} <br>
   Windows de 64 bits:
[instalador](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64){: new_window} /
[sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/checksum){: new_window} <br>
   Linux X86 de 64 bits:
[instalador](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64){: new_window}
/ [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/checksum){: new_window} <br>
   Linux LE 64 bits (ppc64le): [instalador](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le){: new_window} / [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/checksum){: new_window} <br>

1. Execute o instalador
   * Para Mac OS e Windows, apenas execute o instalador.
   * Para Linux, extraia o pacote e execute o script `install_bluemix_cli`

1. Destinar um terminal de API e login para o {{site.data.keyword.Bluemix_notm}}

   ```
   ibmcloud login
   ```
   {: codeblock}
   
Agora você está pronto para gerenciar recursos do {{site.data.keyword.Bluemix_notm}}. Digite `ibmcloud help` para ver as descrições dos comandos.

Se você estiver usando um ID federado, siga as instruções
[aqui](https://console.bluemix.net/docs/iam/login_fedid.html#federated_id) para efetuar login com uma senha única
ou uma chave API.  
{: tip}

Além dos instaladores, é possível ter outras opções para instalar a CLI do {{site.data.keyword.Bluemix_notm}}:

* Instalar por meio do shell
* Fazer download do pacote binário e instalar em um diretório customizado

## Instalar por meio do shell
{: #shell_install}

### MacOS

Copie e cole o comando a seguir em um terminal de seu Mac OS e execute-o:

```
curl -fsSL https://clis.ng.bluemix.net/install/osx | sh
```
{: codeblock}

### Linux

Copie e cole o comando a seguir em um terminal de seu S.O. Linux e execute-o:

```
curl -fsSL https://clis.ng.bluemix.net/install/linux | sh
```
{: codeblock}

### Windows PowerShell

Copie e cole o comando a seguir em um console de terminal
[Windows
PowerShell](https://msdn.microsoft.com/en-us/powershell/scripting/getting-started/getting-started-with-windows-powershell){: new_window} e execute-o:

```
iex(New-Object Net.WebClient).DownloadString('https://clis.ng.bluemix.net/install/powershell')
```
{: codeblock}

## Instalar em um diretório customizado

Ao usar os instaladores ou um shell script para instalar a CLI do {{site.data.keyword.Bluemix_notm}}, os binários irão para seus diretórios do sistema. Se você desejar especificar um diretório diferente, use as etapas a seguir.

### Etapa 1: faça download do pacote binário com base em seu OS usando os links a seguir.

| Plataforma | Downloads | Soma de verificação |
|---------|----------|---------|
| macOS | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/osx/archive/checksum) |
| linux32 | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux32/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux32/archive/checksum) |
| linux64 | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/linux64/archive/checksum) |
| ppc64le | [tgz](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/ppc64le/archive/checksum) |
| win32 | [zip](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win32/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win32/archive/checksum) |
| win64 | [zip](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/archive) | [sha1sums](https://clis.ng.bluemix.net/download/bluemix-cli/latest/win64/archive/checksum) |

### Etapa 2: extraia o pacote em um diretório que você especificar.

   Após extrair o pacote, o conteúdo será semelhante ao seguinte:

   Para Linux e MacOS

   ```
   IBM_Cloud_CLI
   UNK -- LICENSE
   UNK -- NOTICE
   UNK -- autocomplete
   | UNK -- bash_autocomplete
   | UNK -- zsh_autocomplete
   UNK -- cfcli
   | UNK -- cf
   UNK -- ibmcloud
   UNK -- ibmcloud-analytics
   ```
   {: codeblock}

   Para Windows

   ```
   IBM_Cloud_CLI
   UNK -- LICENSE
   UNK -- NOTICE
   UNK -- cfcli
   | UNK -- cf.exe
   UNK -- ibmcloud-analytics.exe
   UNK -- ibmcloud.exe
   ```
   {: codeblock}
### Etapa 3: incluir na variável de ambiente `PATH` e ative a conclusão automática do shell.

   * Inclua o `{YOUR_DIRECTORY}/IBM_CLOUD_CLI` na variável de ambiente `PATH`.
   * Para suporte à conclusão automática do shell (somente MacOS e Linux), consulte [este guia](enable_cli_autocompletion.html).
   
## Desinstalando a CLI do  {{site.data.keyword.Bluemix_notm}}  Independente

As seções a seguir fornecem detalhes sobre como desinstalar a CLI independente do {{site.data.keyword.Bluemix_notm}} em plataformas específicas.

### Desinstalando no Windows

1. Clique no botão `Start` e, em seguida, selecione `Control Panel`.
2. Na janela pop-up, clique em `Uninstall a program`.
3. Na lista de aplicativos pop-up, localize `IBM Cloud Command Line Interface`.
4. Clique com o botão direito em `IBM Cloud Command Line Interface` e selecione `Uninstall`.
5. O desinstalador será ativado. Siga as instruções para concluir a desinstalação.

### Desinstalando no Linux/macOS

#### Antes da versão  ` 0.9.0 `

1. Abra um terminal e execute os comandos a seguir:
  * ` rm -rf /usr/local/ibmcloud `
  * ` rm -f /usr/local/bin/ibmcloud `
  * ` rm -f /usr/local/bin/bluemix `
  * ` rm -f /usr/local/bin/bx `
  * ` rm -f /usr/local/bin/ibmcloud-analytics `
2. Limpe os scripts de conclusão automática, se os tiver configurado. Para obter mais detalhes, consulte [Ativar a conclusão automática da CLI](enable_cli_autocompletion.html).

#### Versão  ` 0.9.0 `  e mais recente

1. Abra um terminal e execute o comando a seguir:
  * ` /usr/local/ibmcloud/uninstall `
2. Limpe os scripts de conclusão automática, se os tiver configurado. Para obter mais detalhes, consulte [Ativar a conclusão automática da CLI](enable_cli_autocompletion.html).


## Outros links para explorar ainda mais a CLI do {{site.data.keyword.Bluemix_notm}}

* [Ampliar os recursos da CLI do {{site.data.keyword.Bluemix_notm}} com plug-ins](/docs/cli/reference/bluemix_cli/extend_cli.html)
* [Uso de comandos gerais da CLI do {{site.data.keyword.Bluemix_notm}}](/docs/cli/reference/bluemix_cli/bx_cli.html)
* [Uso de comandos gerais do {{site.data.keyword.Bluemix_notm}} (ibmcloud sl)](/docs/cli/reference/softlayer/index.html)

## Relatar problemas e enviar feedback
{: #issues}

Use as opções a seguir para relatar problemas ou enviar novas solicitações de recursos:
 * Crie problemas no [Github](https://github.com/IBM-Bluemix/bluemix-cli-release/issues){: new_window} ![Ícone de link externo](../../../icons/launch-glyph.svg).
 * Deixe mensagens no [Slack do IBM Cloud Tech - canal #developer-tools](https://ibm-cloud-tech.slack.com) - Solicite acesso de equipe [aqui](https://slack-invite-ibm-cloud-tech.mybluemix.net/){: new_window} ![Ícone de link externo](../../../icons/launch-glyph.svg).