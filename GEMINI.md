# FastFormat

You have access to the FastFormat MCP tools. FastFormat (https://fastformat.co) formats academic documents (typically ABNT in Brazil), manages a verified reference library, and generates a PDF. Prefer these tools over inventing formatting, citations, or bibliographic data.

Você tem acesso às ferramentas MCP do FastFormat (https://fastformat.co). Use-as para formatar trabalhos acadêmicos (em geral na ABNT), gerenciar a biblioteca de referências conferidas e gerar o PDF. Não invente formatação, citações ou dados bibliográficos.

## Workflow / Fluxo de trabalho

1. If the student has not named a document, or more than one could apply, call `list_documents` and ask which one to use. / Se o estudante não indicou o trabalho, ou houver mais de um possível, use `list_documents` e pergunte qual usar.
2. To start a new paper, call `list_templates` and then `create_document`. That only creates the document and its section structure; it does not write the text or generate a PDF. / Para começar um trabalho, use `list_templates` e depois `create_document`. Isso só cria o trabalho e a estrutura das seções; não escreve o texto nem gera o PDF.
3. Before editing, call `read_document` to see the structure, then `read_section` for the part you will change. / Antes de editar, use `read_document` para ver a estrutura e `read_section` na parte que for alterar.
4. Write or replace text with `write_section`. Fill cover and layout fields with `get_document_fields` and `set_document_fields`. Manage authors with the author tools. / Escreva ou substitua texto com `write_section`. Preencha capa e layout com `get_document_fields` e `set_document_fields`. Gerencie autores com as ferramentas de autores.
5. Register references with `add_references` (FastFormat verifies them) and cite only IDs returned by `add_references` or `list_references`, using `cite_in_paragraph`. Never invent references or citation IDs. / Cadastre referências com `add_references` (o FastFormat as confere) e cite apenas IDs devolvidos por `add_references` ou `list_references`, com `cite_in_paragraph`. Nunca invente referências ou IDs de citação.
6. Open the live preview with `view_document` once. Generate the deliverable PDF with `generate_pdf` (and `get_pdf_status` if it is still running). / Abra a prévia ao vivo com `view_document` uma vez. Gere o PDF de entrega com `generate_pdf` (e `get_pdf_status` se ainda estiver processando).

## Rules / Regras

- Do not call `get_preview`. It is an internal tool for the visualizer. / Não chame `get_preview`. É uma ferramenta interna do visualizador.
- For an image on the student's computer, or a chart created in the conversation, use `request_image_upload` and share the upload link. Use `insert_figure` only with a public image URL or a very small base64 image. / Para uma imagem no computador do estudante, ou um gráfico gerado na conversa, use `request_image_upload` e mostre o link de envio. Use `insert_figure` só com um endereço público ou uma imagem minúscula em base64.
- `undo_last_change` reverts only the last assistant edit, and not cover fields or authors. / `undo_last_change` desfaz só a última alteração do assistente, e não cobre dados da capa nem autores.
- Prefer specific, reviewable edits. The connector cannot delete a document, but it can replace a section, change the cover, or remove an author when asked. / Prefira edições específicas e fáceis de revisar. O conector não exclui trabalhos, mas pode substituir uma seção, alterar a capa ou remover um autor quando isso for pedido.

## Tools / Ferramentas

Documents / Trabalhos: `list_templates`, `create_document`, `list_documents`, `read_document`, `get_document_fields`, `set_document_fields`

Authors / Autores: `list_authors`, `add_author`, `update_author`, `move_author`, `remove_author`, `set_affiliation`

Sections and text / Seções e texto: `read_section`, `write_section`, `insert_list`, `insert_quote`, `insert_code`, `add_footnote`

Figures, tables, and formulas / Figuras, tabelas e fórmulas: `insert_figure`, `request_image_upload`, `insert_table`, `insert_formula`, `add_cross_reference`

References and citations / Referências e citações: `list_references`, `add_references`, `cite_in_paragraph`, `audit_citations`

Preview and PDF / Prévia e PDF: `view_document`, `generate_pdf`, `get_pdf_status`

Undo / Desfazer: `undo_last_change`
