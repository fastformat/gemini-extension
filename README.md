# FastFormat for Gemini CLI

<p align="center">
  <img src="https://fastformat.co/.well-known/mcp/icon-512.png" alt="FastFormat" width="128" height="128">
</p>

Gemini CLI extension for the [FastFormat](https://fastformat.co) remote MCP server. Format academic documents (ABNT), add verified bibliographic references, and generate a PDF from your FastFormat account.

Extensão do Gemini CLI para o servidor MCP remoto do [FastFormat](https://fastformat.co). Formate trabalhos acadêmicos (ABNT), cadastre referências bibliográficas conferidas e gere o PDF a partir da sua conta FastFormat.

## English

### What it is

This repository is a small public wrapper so you can install FastFormat in [Gemini CLI](https://geminicli.com) with one command. The tools themselves run on FastFormat's remote MCP server at `https://fastformat.co/mcp` (Streamable HTTP, OAuth 2.1). You need a [FastFormat](https://fastformat.co) account. The connector is available on every plan; on the free plan, generated PDFs may include a watermark.

### Install

You need [Gemini CLI](https://geminicli.com) and `git`.

```bash
gemini extensions install https://github.com/fastformat/gemini-extension
```

Restart Gemini CLI after installing. To update later:

```bash
gemini extensions update fastformat
```

### Sign in

The first time the tools are used, Gemini CLI discovers OAuth automatically. In Gemini CLI, run:

```text
/mcp auth fastformat
```

A browser window opens so you can sign in to FastFormat and authorize access. Your password stays with FastFormat; the CLI receives only an access token. To disconnect later, revoke access in FastFormat under **Account → Connected apps**, and uninstall or disable the extension in Gemini CLI.

### Learn more

- Connector guide: [fastformat.co/conector](https://fastformat.co/conector)
- Privacy policy: [app.fastformat.co/privacy](https://app.fastformat.co/privacy)
- Terms of use: [app.fastformat.co/tos](https://app.fastformat.co/tos)
- Support: [suporte@fastformat.com.br](mailto:suporte@fastformat.com.br)

## Português

### O que é

Este repositório é um invólucro público pequeno para instalar o FastFormat no [Gemini CLI](https://geminicli.com) com um comando. As ferramentas rodam no servidor MCP remoto do FastFormat, em `https://fastformat.co/mcp` (Streamable HTTP, OAuth 2.1). É preciso ter uma [conta FastFormat](https://fastformat.co). O conector está disponível em todos os planos; no plano gratuito, o PDF gerado pode ter marca d'água.

### Instalação

É necessário ter o [Gemini CLI](https://geminicli.com) e o `git`.

```bash
gemini extensions install https://github.com/fastformat/gemini-extension
```

Reinicie o Gemini CLI depois de instalar. Para atualizar depois:

```bash
gemini extensions update fastformat
```

### Login

Na primeira vez que as ferramentas forem usadas, o Gemini CLI descobre o OAuth automaticamente. No Gemini CLI, rode:

```text
/mcp auth fastformat
```

O navegador abre para você entrar no FastFormat e autorizar o acesso. A senha permanece no FastFormat; o CLI recebe só um token de acesso. Para desconectar depois, revogue o acesso no FastFormat em **Conta → Apps conectados** e desinstale ou desative a extensão no Gemini CLI.

### Saiba mais

- Página do conector: [fastformat.co/conector](https://fastformat.co/conector)
- Política de Privacidade: [app.fastformat.co/privacy](https://app.fastformat.co/privacy)
- Termos de Uso: [app.fastformat.co/tos](https://app.fastformat.co/tos)
- Suporte: [suporte@fastformat.com.br](mailto:suporte@fastformat.com.br)

## License

[MIT](LICENSE) © FastFormat
