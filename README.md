# Júlia & Guilherme — convite de casamento

## Configurar o Supabase

1. Crie um projeto no Supabase.
2. No SQL Editor do projeto, execute [`supabase/migrations/20261001000000_create_wedding_rsvps.sql`](./supabase/migrations/20261001000000_create_wedding_rsvps.sql).
3. Copie `.env.example` para `.env.local` e preencha `VITE_SUPABASE_URL` e `VITE_SUPABASE_ANON_KEY` com os dados do projeto.
4. Reinicie o servidor de desenvolvimento com `npm run dev`.

O formulário grava nome, telefone e mensagem na tabela `public.wedding_rsvps`. A política de Row Level Security permite inserções públicas para o formulário, mas não permite que visitantes leiam as confirmações. Use somente a chave anon/publishable no frontend; nunca coloque a `service_role` key em variáveis `VITE_*`.

Sem as variáveis de ambiente, o formulário explica que a conexão ainda precisa ser configurada e não tenta enviar os dados.

## Desenvolvimento

```sh
npm install
npm run dev
```

Para gerar a versão de produção, execute `npm run build`.
