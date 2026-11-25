# MANGÁ ESTE

Plataforma de mangás autorais em desenvolvimento, com leitura online, painel de publicação e loja com pagamento PIX.

## Situação
O repositório contém a documentação inicial. O pacote de aplicação completo está sendo preparado separadamente; o site ainda não está publicado nem validado em produção.

## Tecnologias planejadas
- Next.js
- Supabase (autenticação, banco e armazenamento)
- Cloudflare Workers / OpenNext
- Mercado Pago para PIX (pode haver taxas por transação)

## Configuração do pacote
1. Extraia o ZIP do projeto e copie o conteúdo da pasta `manga-este/` para a raiz deste repositório.
2. Instale Node.js 20+ e execute `npm install`.
3. Copie `.env.example` para `.env.local` e preencha as credenciais no ambiente local.
4. Crie o projeto Supabase e execute `supabase/schema.sql` no SQL Editor.
5. Crie sua conta no site e promova somente seu usuário a administrador usando o SQL Editor:
   `update public.profiles set role='admin' where id=(select id from auth.users where email='SEU_EMAIL');`
6. Configure Cloudflare e os segredos com Wrangler; nunca coloque chaves secretas no GitHub.
7. Execute `npm run cf:preview`, teste e só então `npm run cf:deploy`.

## Limitações atuais
Ainda faltam testes completos, histórico/progresso sincronizados, notificações, moderação, recuperação de conta, gestão de produtos e entrega protegida de compras. O pacote inicial não deve ser tratado como produto final de produção. Os planos gratuitos possuem limites e podem mudar.

Consulte `SECURITY.md` antes de configurar credenciais ou receber pagamentos.
