# Avistar 2026 · Gerador de Certificados

Página estática hospedada no GitHub Pages para emissão de certificados on-demand.

## Estrutura do repositório

```
avistar2026/
├── index.html                  ← página principal (este repo)
├── certificados.pdf            ← PDF base com layout/assinatura
├── inscritos.json              ← base de participantes (por e-mail)
├── inscritos_por_nome.json     ← base de participantes (por nome, fallback)
├── palestrantes.json           ← base de trabalhos apresentados
├── Ubuntu-Regular.ttf          ← fonte
├── Ubuntu-Bold.ttf             ← fonte
└── README.md
```

## Como fazer o deploy

1. Crie o repositório `avistar2026` no GitHub (conta `gutocarv`)
2. Copie todos os arquivos desta pasta para o repositório
3. No GitHub: **Settings → Pages → Source → Deploy from branch → main → / (root)**
4. Aguarde ~2 minutos → acesse: `https://gutocarv.github.io/avistar2026/`

## Fluxo do usuário

1. Digita o e-mail → sistema busca em `inscritos.json` e `palestrantes.json`
2. Se encontrado → exibe botões de download para cada certificado disponível
3. Se não encontrado → exibe campo de busca por nome (fallback para os 85 sem e-mail)
4. O PDF é gerado 100% no browser → download automático, zero servidor

## Atualizar a base

Para atualizar os dados (novos inscritos, correções):
- Substitua os arquivos `.json` no repositório
- O GitHub Pages serve a versão mais recente automaticamente

## Certificados gerados

| Tipo | Fonte dos dados |
|------|----------------|
| Participação (Congressista, Expositor, Staff...) | `inscritos.json` |
| Apresentação (Palestra, Pôster, Oficina...) | `palestrantes.json` |
