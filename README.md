# Projeto Azure Translator

Este repositório foi desenvolvido como parte do curso de Azure Translator (DIO).  
Ele demonstra como utilizar o serviço de tradução da Microsoft Azure no Google Colab para diferentes cenários:

- Tradução de **texto simples**
- Tradução de **arquivos Word (.docx)**
- Tradução de **conteúdo de sites**

---

## Estrutura do projeto
- `translate_docx.ipynb` → tradução de arquivos Word usando `python-docx` e Azure Translator.
- `translate_text_site.ipynb` → extração de texto de páginas web com `BeautifulSoup` e tradução usando Azure OpenAI.
- (Opcional) `translate_text.ipynb` → exemplo de tradução de texto simples.

---

## Pré-requisitos
- Conta na [Microsoft Azure](https://azure.microsoft.com/).
- Recurso **Translator** criado no portal da Azure.
- Chave de API e região do recurso.
- (Opcional) Recurso **Azure OpenAI** para tradução de artigos e sites.

---

## Como usar
1. Abra o notebook no Google Colab.
2. Instale as dependências necessárias:
   ```bash
   !pip install requests python-docx beautifulsoup4 openai langchain-openai
3. Substitua os placeholders no código:

"YOUR_KEY_HERE" → sua chave do Azure Translator ou Azure OpenAI.
"YOUR_REGION_HERE" → região do recurso (ex.: eastus2).
"LINGUAGE_TO_TRANSLATE" → idioma de destino (ex.: pt).
"YOUR_ENDPOINT_HERE" → endpoint do recurso Azure OpenAI.
"YOUR_DEPLOYMENT_NAME" → nome do deployment configurado no Azure OpenAI.
"YOUR_FILE_DIRECTORY" → caminho do arquivo .docx a ser traduzido.
"ADD_WEBSITE_LINK_HERE" → URL do site a ser traduzido.
4. Execute as células para realizar as traduções.

Observação
As chaves da Azure não estão incluídas neste repositório por motivos de segurança.
Cada usuário deve gerar sua própria chave no portal da Azure e substituir os placeholders no código.
O repositório contém apenas exemplos de uso e não expõe credenciais reais.

### Exemplos de uso ###
Tradução de texto simples:

python
translator_text("I love you, I love you", "pt")
Tradução de documento Word:

python
translate_document("meuarquivo.docx")

Tradução de site:
python
text = extract_text_from_url("https://exemplo.com")
article = translate_article(text, "pt-br")
print(article)
