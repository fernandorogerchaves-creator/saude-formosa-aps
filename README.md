# Saúde Formosa APS

Portal da Atenção Primária à Saúde de Formosa-GO.

**Versão 1.0**

Esta versão publica as ferramentas que funcionam de forma estática. Recursos que dependem de banco de dados, autenticação no servidor, permissões institucionais ou persistência longitudinal permanecem identificados como **Em construção** e com acesso restrito.

Domínio planejado: https://saude-formosa-aps.com.br

## Segurança

Este repositório é publicado como site estático no GitHub Pages. Ele não contém backend, banco de dados, controladores HTTP ou criação de cookies. Portanto, autenticação real, cookies de sessão com `Secure`/`HttpOnly`/`SameSite`, validação server-side com HTTP 400 e prepared statements só podem ser implementados quando houver um servidor de aplicação.

A área profissional desta versão usa apenas identificação local de interface, com expiração em `sessionStorage`; ela não deve ser tratada como controle de acesso. O site não coleta senha nessa etapa. Recursos que exigem autenticação, persistência ou autorização institucional devem permanecer bloqueados até existir backend apropriado.

No cliente há defesa em profundidade: CSP por `meta`, política de referrer, validação de rotas e formulários, sanitização/limite de payloads antes de POSTs externos e mensagens genéricas de erro. Cabeçalhos HTTP de segurança que dependem do servidor devem ser configurados na camada de hospedagem/reverse proxy caso o site migre do GitHub Pages.
