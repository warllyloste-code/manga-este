# MANGÁ ESTE

Plataforma de mangás autorais em desenvolvimento, com catálogo, leitura online, painel de publicação e loja com PIX.

## Situação real
O repositório contém documentação. O código-fonte completo está no pacote ZIP disponibilizado nesta conversa, mas ainda não foi transferido para este repositório. O site não está publicado e não foi possível concluir o build local porque o ambiente não conseguiu acessar o registro npm.

## Stack
- Next.js
- Supabase (autenticação, banco e armazenamento)
- Cloudflare Workers / OpenNext
- Mercado Pago para PIX (pode haver taxas por transação)

## Preparação do código
1. Extraia o ZIP e copie o conteúdo de `manga-este/` para a raiz do repositório.
2. Instale Node.js 20+ e rode `npm install`.
3. Copie `.env.example` para `.env.local`.
4. Crie um projeto Supabase e execute `supabase/schema.sql` no SQL Editor.
5. Depois de criar sua conta, promova somente seu usuário a administrador no SQL Editor: `update public.profiles set role='admin' where id=(select id from auth.users where email='SEU_EMAIL');`
6. Configure os segredos no Cloudflare/Wrangler; nunca publique chaves secretas no Git.
7. Rode `npm run cf:preview`, teste e só depois `npm run cf:deploy`.

## O que ainda falta
Testes completos, histórico/progresso sincronizados, notificações, moderação, recuperação de conta, gestão de produtos e entrega protegida de compras. O pacote é um protótipo em desenvolvimento, não um produto pronto para produção. Os planos gratuitos têm limites e podem mudar.

Consulte `SECURITY.md` antes de configurar credenciais ou pagamentos.
