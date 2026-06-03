# Setting Up GitHub Public Repo

Step-by-step para criar e popular o repositório público `terra-concordia` no GitHub.

---

## 1. Criar Organization GitHub (recomendado)

```
1. Acessar https://github.com/organizations/new
2. Nome: ncbgames (igual ao domínio)
3. Email: terraconcordia@ncbgames.com
4. Plan: Free
5. Confirmar
```

Vantagens de Org:
- Separa pessoal do business
- Permite múltiplos repos da NCB Company
- Profissional aos olhos da comunidade

## 2. Criar Repositório

```
1. github.com/ncbgames → New Repository
2. Nome: terra-concordia
3. Descrição: "Public materials for Terra Concordia — A digital eurogame by NCB Company"
4. Public ✅
5. Add README ✅
6. Add .gitignore: None (criamos manualmente)
7. Choose license: Creative Commons Zero v1.0 ("CC0-1.0")
   OU upload custom CC BY-NC 4.0
8. Create repository
```

## 3. Configurar Branches

```
git clone git@github.com:ncbgames/terra-concordia.git
cd terra-concordia

# Copiar conteúdo de github-public/
cp -r /path/to/TerraConcordiaSteam/github-public/* .

# Estrutura
mkdir -p press-kit/screenshots
mkdir -p press-kit/logos
mkdir -p achievement-icons
mkdir -p capsule-arts/en
mkdir -p capsule-arts/pt
mkdir -p capsule-arts/es
mkdir -p capsule-arts/zh-Hans
mkdir -p release-notes
mkdir -p community
mkdir -p logos

# Copiar assets
cp /path/to/TerraConcordiaSteam/press-kit/* press-kit/
cp /path/to/TerraConcordiaSteam/screenshots/*.png press-kit/screenshots/
cp /path/to/TerraConcordiaSteam/steam-integration/achievements/icons/*.png achievement-icons/
cp -r /path/to/TerraConcordiaSteam/store-assets/capsules/B-gameplay/*/* capsule-arts/

# Commit
git add .
git commit -m "Initial public release: press kit + achievements + capsules"
git push
```

## 4. Configurar Settings do Repo

### Geral
- Issue tracker: enabled
- Discussions: enabled
- Wiki: disabled (use GitHub Pages se quiser)
- Projects: disabled (use Discord)

### Branches
- Default: `main`
- Branch protection: require PR for changes (opcional)

### Pages (opcional)
Para hospedar press kit no GitHub Pages:

```
Settings → Pages
Source: Deploy from branch
Branch: main / press-kit
URL: ncbgames.github.io/terra-concordia/press-kit/
```

Alternativa: usar HostGator com ncbgames.com/press-kit (já planejado).

### Issue Templates

Criar `.github/ISSUE_TEMPLATE/`:
- `bug_report.md`
- `feature_request.md`
- `translation_request.md`

(Templates já em `community/CONTRIBUTING.md`, basta copiar.)

### Code Owners

`.github/CODEOWNERS`:
```
# NCB approves all changes
* @ncbgames-admin
```

## 5. Adicionar GitHub Actions (CI/CD)

Para validar PRs automaticamente:

`.github/workflows/validate.yml`:
```yaml
name: Validate
on: [pull_request]
jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Validate markdown
        run: |
          npx markdownlint-cli '**/*.md' --config .markdownlint.json
      - name: Validate image dimensions
        run: |
          # Custom script para garantir achievement icons são 64x64
```

## 6. Promover

### Adicionar topics
GitHub topics ajudam discovery:
- `game-development`
- `indie-game`
- `eurogame`
- `strategy-game`
- `steam`
- `civilization-game`
- `boardgame`
- `solo-dev`
- `brazil-indie`

### Star o repo
Pedir Discord members para ⭐ o repo:
- Aumenta visibility no GitHub trending
- Sinal de comunidade ativa

### Cross-link
- Steam page: link para GitHub
- ncbgames.com: link para GitHub
- Press kit: link para GitHub

## 7. Cadência de Updates

Atualizar GitHub público quando:
- ✅ Hot fix released → adicionar release notes
- ✅ Patch released → atualizar `release-notes/`
- ✅ New screenshots → adicionar em `press-kit/screenshots/`
- ✅ Press kit atualizado → push para `press-kit/`

NÃO atualizar com cada commit privado. Só releases públicas.

---

## ✅ Checklist Inicial

- [ ] Org `ncbgames` criada
- [ ] Repo `terra-concordia` criado (public)
- [ ] README.md inicial
- [ ] LICENSE.md (CC BY-NC 4.0 para assets, MIT para code/docs)
- [ ] Issue templates
- [ ] Topics adicionados
- [ ] Pinned no perfil de @ncbgames
- [ ] Link no Steam community hub
- [ ] Link no Discord #welcome
- [ ] Link no ncbgames.com footer

---

**Tempo total estimado:** 1-2 horas para setup completo.
