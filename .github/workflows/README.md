# GitHub Actions Workflows

## Publish to Wiki

Workflow: `publish-to-wiki.yml`

### Čo robí

Automaticky publikuje súbor `v2/index.html` na GitHub Wiki repozitára pri každej zmene.

### Ako to funguje

1. **Spúšťa sa automaticky** keď:
   - Pushujete zmeny do `main` vetvy
   - Zmení sa súbor `v2/index.html`

2. **Alebo manuálne**:
   - Prejdite na: `Actions` → `Publish to Wiki` → `Run workflow`

3. **Proces**:
   - Naklonuje Wiki repozitár
   - Skopíruje `v2/index.html` ako `Hra-na-agenta.html`
   - Vytvorí markdown wrapper stránku `Hra-na-agenta.md`
   - Commitne a pushne zmeny do Wiki

### Nastavenie

#### Krok 1: Povoľte Wiki

1. Prejdite do repozitára na GitHub
2. Kliknite na `Settings` → `Features`
3. Zapnite `Wikis`

#### Krok 2: Inicializujte Wiki

1. Kliknite na záložku `Wiki` vo vašom repozitári
2. Vytvorte prvú stránku (napr. "Home")
3. To vytvorí Wiki git repozitár

#### Krok 3: Povoľte Write prístup pre GitHub Actions

1. Prejdite na `Settings` → `Actions` → `General`
2. Nájdite sekciu `Workflow permissions`
3. Vyberte `Read and write permissions`
4. Uložte zmeny

#### Krok 4: Commitnite a pushnite workflow

```bash
git add .github/workflows/publish-to-wiki.yml
git commit -m "Add GitHub Action to publish to Wiki"
git push origin main
```

### Použitie

Po každom pushnutí zmien v `v2/index.html`:

1. Workflow sa spustí automaticky
2. Po dokončení (1-2 minúty) navštívte:
   - **Wiki stránka**: `https://github.com/USERNAME/REPO/wiki/Hra-na-agenta`
   - **Priama HTML**: `https://github.com/USERNAME/REPO/wiki/Hra-na-agenta.html`

### Riešenie problémov

**Workflow zlyhá s "permission denied"**
- Skontrolujte, či má GitHub Actions write prístup (Krok 3 vyššie)
- Overte, že Wiki je inicializovaná (Krok 2 vyššie)

**Wiki sa neaktualizuje**
- Skontrolujte `Actions` záložku pre logy
- Overte, že ste zmenili súbor v ceste `v2/index.html`
- Skúste manuálne spustiť workflow

**HTML sa nezobrazuje správne**
- GitHub Wiki môže mať obmedzenia pre inline HTML
- Alternatíva: Použite GitHub Pages namiesto Wiki

### GitHub Pages alternatíva

Ak Wiki nefunguje kvôli obmedzeniam HTML:

1. Povoľte GitHub Pages:
   - `Settings` → `Pages`
   - Source: `Deploy from a branch`
   - Branch: `main` → folder: `/v2`

2. Aplikácia bude dostupná na:
   - `https://USERNAME.github.io/REPO/v2/index.html`

### Poznámky

- Workflow používa `GITHUB_TOKEN` ktorý je automaticky dostupný
- Žiadne dodatočné secrets nie sú potrebné
- Wiki repozitár je samostatný git repozitár na: `https://github.com/USERNAME/REPO.wiki.git`
