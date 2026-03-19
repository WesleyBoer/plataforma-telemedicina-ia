# Clínica Reaviva — Plataforma Customizada de Telemedicina com IA

Plataforma web full-stack desenvolvida **exclusivamente sob medida** para a Clínica Reaviva (especializada em psiquiatria). Centraliza 100% da operação da clínica: agenda médica, videoconferências seguras sem apps externos, gestão de pacientes, pagamentos (PIX/cartão), geração automática de prontuários via IA, assinatura digital com validade jurídica (ICP-Brasil) e emissão automática de NFS-e.

**Projeto confidencial** — código-fonte privado. Este repositório existe apenas como showcase técnico e referência para o case study detalhado.

## Impacto Real Entregue ao Cliente

| Métrica                              | Resultado          |
|--------------------------------------|--------------------|
| Redução de custos operacionais       | **80%**            |
| Centralização da operação            | **100%**           |
| Consultas realizadas na plataforma   | **+1.000**         |

> "Finalmente tínhamos algo totalmente adaptado para nossa empresa, que centralizava nossa operação, reduziu em pelo menos 80% nossos custos e ainda estava pronto para escalar."  
> — **Lucas Rodrigues**, Sócio-fundador · Clínica Reaviva

## Problema resolvido

Antes: fragmentação entre múltiplas ferramentas (videoconferência externa, agenda separada, pagamentos em outro sistema, prontuários manuais) → alto custo, baixa eficiência e alternância constante de sistemas.

Depois: única plataforma integrada que atende médicos, pacientes e administração, com automações inteligentes baseadas em IA.

## Stack Tecnológico Principal

**Frontend**  
Next.js 16 · React · TypeScript · shadcn/ui + Radix UI · Tailwind CSS

**Backend & Microserviços**  
Python + FastAPI (transcrição de áudio)  
Bun + TypeScript (geração de prontuários)  
RabbitMQ (filas assíncronas)

**Banco de Dados & Cache**  
PostgreSQL · Prisma ORM (50+ modelos) · Redis

**Videoconferência**  
LiveKit (WebRTC) — salas seguras sem instalação de aplicativos

**Inteligência Artificial**  
OpenAI Whisper (Speech-to-Text)  
OpenAI GPT-4o-mini (estruturação de prontuários)  
LangChain + RAG (sistema Oráculo interno)

**Pagamentos & Fiscal**  
Asaas (PIX, cartão parcelado)  
Spedy (emissão automática NFS-e)

**Compliance & Segurança**  
ICP-Brasil / IntegraICP (assinatura digital PAdES)  
Autenticação passwordless via WhatsApp OTP  
RBAC granular (dezenas de níveis de permissão)  
Privacidade-by-design (anonimização PII antes de IA – LGPD/HIPAA)

**Infraestrutura**  
AWS EC2 (on-demand auto-scaling) · Docker · Nginx · Sentry

## Destaques de Arquitetura e Decisões Técnicas

- Microserviços on-demand: pipeline de IA só consome recursos durante consultas ativas
- Pipeline assíncrono completo: transcrição → anonimização → geração de prontuário → revisão médica
- Autenticação sem senha (OTP via WhatsApp) + controle de acesso extremamente granular
- Integrações fiscais e jurídicas brasileiras nativas (Asaas, Spedy, ICP-Brasil)
- Sistema de RAG próprio (Oráculo) para consultas semânticas sobre dados clínicos e operacionais
- Feedback inteligente pós-consulta com direcionamento automático para Google Reviews (nota 5)

## Case Study Completo

Diagramas de arquitetura (ReactFlow), fluxo detalhado da consulta, pipeline de IA, métricas técnicas, depoimentos e mais de 37 screenshots:  
👉 https://wboer.dev/project/clinica-reaviva

## Aplicação em Produção

https://app.clinicareaviva.com.br  
(Acesso restrito a equipe médica, administrativa e pacientes autorizados)

Projeto confidencial — detalhes adicionais disponíveis apenas em entrevistas ou sob acordo de confidencialidade.

Tecnologias chave: Next.js · TypeScript · Python · FastAPI · OpenAI · LiveKit · RabbitMQ · AWS · Prisma · ICP-Brasil · telemedicina · IA em saúde
