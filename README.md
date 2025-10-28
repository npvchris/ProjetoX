# 🚗 AutoEscola Conecta - Sistema de Instrutores Autônomos

Plataforma moderna e futurística para conectar instrutores de trânsito autônomos com alunos que procuram aulas práticas na sua região.

## 🎯 Sobre o Projeto

**AutoEscola Conecta** é um MVP (Minimum Viable Product) que permite:

### 👨‍🏫 Para Instrutores (Clientes Pagantes)
- ✅ Cadastro profissional com documentação (CNH, registro, comprovantes)
- ✅ Perfil público com avaliações e reputação
- ✅ Sistema de créditos e assinaturas mensais
- ✅ Recebimento de contatos de alunos interessados
- ✅ Dashboard completo com estatísticas

### 🎓 Para Alunos (Usuários Gratuitos)
- ✅ Busca por localização (GPS ou endereço)
- ✅ Visualização de perfis com avaliações
- ✅ Contato direto via WhatsApp
- ✅ Sistema de avaliações

## 🚀 Tecnologias Utilizadas

- **Frontend**: React 18 + TypeScript + Vite
- **Estilização**: Tailwind CSS (tema futurístico com azul, vermelho e branco)
- **Backend**: Supabase (PostgreSQL + Auth + RLS)
- **Ícones**: Lucide React
- **Deploy**: Hostinger (compatível)

---

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter instalado:

- **Node.js** (versão 18 ou superior)
- **npm** ou **yarn**
- **Git**
- Conta no **Supabase** (gratuita)

---

## 🔧 Instalação Local

### 1️⃣ Clone o Repositório

```bash
cd projetox
```

### 2️⃣ Instale as Dependências

```bash
npm install
```

### 3️⃣ Configure as Variáveis de Ambiente

Nao precisa por enquanto 

### 5️⃣ Inicie o Servidor de Desenvolvimento

```bash
npm run dev
```

O aplicativo estará rodando em: **http://localhost:5173**

### 6️⃣ Acesse as Páginas

- **Busca de Instrutores** (alunos): `http://localhost:5173/`
- **Portal do Instrutor**: `http://localhost:5173/instructor`


Seu site estará disponível em:
- `https://seudominio.com/` (busca de instrutores)
- `https://seudominio.com/instructor` (portal do instrutor)

---

## 📁 Estrutura do Projeto

```
project/
├── src/
│   ├── components/          # Componentes reutilizáveis
│   │   ├── InstructorCard.tsx
│   │   ├── SearchBar.tsx
│   │   └── UnlockContactModal.tsx
│   ├── contexts/            # Context API (Auth)
│   │   └── AuthContext.tsx
│   ├── lib/                 # Configurações e tipos
│   │   └── supabase.ts
│   ├── pages/               # Páginas da aplicação
│   │   ├── StudentSearch.tsx
│   │   ├── InstructorDashboard.tsx
│   │   └── AuthPage.tsx
│   ├── App.tsx              # Componente principal
│   ├── main.tsx             # Entry point
│   └── index.css            # Estilos globais
├── .env                     # Variáveis de ambiente
├── package.json
├── vite.config.ts
└── README.md
```

---

## 🗄️ Estrutura do Banco de Dados

### Tabelas Principais

1. **instructors** - Perfis dos instrutores
2. **instructor_documents** - Documentação anexada
3. **subscriptions** - Planos de assinatura
4. **contact_unlocks** - Registro de contatos desbloqueados
5. **reviews** - Avaliações dos instrutores
6. **credit_transactions** - Histórico de créditos

### Segurança (RLS)

Todas as tabelas possuem **Row Level Security** habilitado com políticas específicas:

- ✅ Instrutores só veem seus próprios dados sensíveis
- ✅ Perfis ativos são públicos para busca
- ✅ Documentos são privados
- ✅ Qualquer um pode criar desbloqueios e avaliações

---

## 🎨 Design e UX

### Paleta de Cores

- **Primária**: Azul (#3B82F6) - Confiança e profissionalismo
- **Secundária**: Vermelho (#EF4444) - Energia e ação
- **Neutra**: Branco e tons de cinza - Clareza e modernidade

### Características do Design

- ✨ Gradientes modernos e animações suaves
- 📱 Totalmente responsivo (mobile-first)
- 🎯 Foco na experiência do usuário jovem
- ⚡ Performance otimizada
- 🔒 Feedback visual claro em todas as ações

---

## 🔐 Sistema de Autenticação

### Para Instrutores

1. Acesse `/instructor`
2. Cadastre-se com email e senha
3. Complete seu perfil profissional
4. Aguarde aprovação (status: `pending_approval`)
5. Após aprovado, seu perfil fica visível na busca

### Para Alunos

Não é necessário cadastro! Basta:
1. Buscar instrutores na página inicial
2. Preencher dados para desbloquear contato
3. Conversar diretamente via WhatsApp

---

## 💰 Sistema de Monetização

### Planos de Assinatura (Futuros)

- **Básico**: R$ 29,90/mês + 10 créditos
- **Pro**: R$ 49,90/mês + 30 créditos
- **Premium**: R$ 99,90/mês + créditos ilimitados

### Créditos

- 1 crédito = 1 desbloqueio de contato por aluno
- Créditos podem ser comprados avulsos
- Histórico completo de transações

---
## 📞 Funcionalidades Principais

### 🔍 Busca de Instrutores

- Busca por endereço ou CEP
- Uso de geolocalização do navegador
- Filtros por avaliação
- Ordenação por reputação

### 📱 Desbloqueio de Contato

- Modal intuitivo para captura de dados do aluno
- Integração automática com WhatsApp
- Registro de leads para o instrutor
- Sistema de créditos transparente

### ⭐ Sistema de Avaliações

- Avaliações de 1 a 5 estrelas
- Comentários opcionais
- Cálculo automático de média
- Exibição em tempo real

### 📊 Dashboard do Instrutor

- Estatísticas em tempo real
- Visualização de avaliações recentes
- Gestão de créditos
- Informações de perfil

---

## 🐛 Solução de Problemas

Espaco para nos descutir 


## 🚀 Próximos Passos (Roadmap)

- [ ] Sistema de pagamentos (integração Stripe)
- [ ] Upload de documentos (Supabase Storage)
- [ ] Chat interno entre instrutor e aluno
- [ ] Sistema de agendamento de aulas
- [ ] Painel administrativo
- [ ] Aplicativo mobile (React Native)
- [ ] Notificações push
- [ ] Analytics e relatórios avançados

---

## 📝 Licença

Este projeto é proprietário e está em desenvolvimento.

---

## 👨‍💻 Suporte

Para dúvidas ou problemas:
- Abra uma issue no repositório
- Entre em contato com a equipe de desenvolvimento

---

## 🎉 Contribuição

Este é um projeto MVP. Contribuições são bem-vindas após aprovação da equipe principal.

---

**Desenvolvido com 💙 e ❤️ para revolucionar o mercado de instrutores de trânsito autônomos no Brasil**
