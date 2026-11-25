# Segurança

- Nunca publique `.env.local`, `SUPABASE_SERVICE_ROLE_KEY`, `MERCADOPAGO_ACCESS_TOKEN` ou `MERCADOPAGO_WEBHOOK_SECRET`.
- Promova apenas sua própria conta a administradora pelo SQL Editor do seu Supabase.
- O bucket público `manga-pages` é destinado a imagens de leitura abertas; não use para arquivos pagos protegidos.
- Teste pagamentos no sandbox e valide assinatura, moeda, valor, pedido e liberação de acesso antes de receber pagamentos reais.
- Ative backups, monitore quotas e publique apenas obras com autorização dos titulares dos direitos autorais.
