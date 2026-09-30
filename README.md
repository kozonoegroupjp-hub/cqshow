# CQShow

Aplicação web para criar **見積書** (orçamentos) e **請求書** (faturas), com interface em português e PDF em japonês. O aplicativo é responsivo e pode ser instalado como atalho no celular.

## Fluxo

1. Entre com e-mail e senha.
2. Complete **Ajustes** com os dados do emissor e da conta bancária.
3. Cadastre clientes e serviços uma vez.
4. Crie um orçamento, altere itens e gere PDF.
5. Abra o orçamento e use **Transformar em fatura**. O orçamento original fica preservado.
6. Gere o PDF japonês da fatura e salve/imprima.

## Segurança

- Autenticação por e-mail e senha do Supabase.
- Regras RLS impedem que a conta conectada leia ou edite dados de outra empresa.
- O navegador usa somente a chave pública (`anon`). A chave `service_role` jamais deve ser colocada neste projeto.

## Publicação gratuita

O destino é GitHub Pages. Antes de publicar, preencher `config.js` com a URL do projeto e sua **Publishable key** do Supabase. Depois, ativar GitHub Pages na raiz do repositório.

O PDF é criado localmente no navegador ao usar o botão PDF; nenhum dado do cliente é enviado a um serviço de PDF externo.
