# Contributing to RoomMate App

> **[🇮🇹 Leggi in Italiano](#contribuire-italiano)** | **🇬🇧 English**

---

First off, thank you for considering contributing to RoomMate App! It's people like you that make this project better.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)
- [Code Contributions](#code-contributions)
- [Style Guidelines](#style-guidelines)
- [Commit Messages](#commit-messages)
- [Pull Request Process](#pull-request-process)

---

## 📜 Code of Conduct

This project and everyone participating in it is governed by our Code of Conduct. By participating, you are expected to uphold this code. Please report unacceptable behavior to andreabonacci95@protonmail.com.

### Our Standards

**Positive behavior includes:**
- Using welcoming and inclusive language
- Being respectful of differing viewpoints and experiences
- Gracefully accepting constructive criticism
- Focusing on what is best for the community
- Showing empathy towards other community members

**Unacceptable behavior includes:**
- Trolling, insulting/derogatory comments, and personal or political attacks
- Public or private harassment
- Publishing others' private information without explicit permission
- Other conduct which could reasonably be considered inappropriate

---

## 🤝 How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

**Bug Report Template:**

```markdown
**Describe the bug**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Environment:**
 - OS: [e.g. Windows 10, macOS 12, Ubuntu 22.04]
 - Browser: [e.g. Chrome 120, Firefox 121, Safari 17]
 - App Version: [e.g. 1.0.0]
 - Device: [e.g. Desktop, iPhone 12, Samsung Galaxy S21]

**Additional context**
Add any other context about the problem here.
```

### Suggesting Features

Feature suggestions are welcome! Before creating a feature request:

1. Check if the feature has already been suggested
2. Make sure it aligns with the project's goals
3. Provide a clear use case

**Feature Request Template:**

```markdown
**Is your feature request related to a problem?**
A clear and concise description of what the problem is. Ex. I'm always frustrated when [...]

**Describe the solution you'd like**
A clear and concise description of what you want to happen.

**Describe alternatives you've considered**
A clear and concise description of any alternative solutions or features you've considered.

**Additional context**
Add any other context or screenshots about the feature request here.

**Would you like to implement this feature?**
Let us know if you're interested in working on this!
```

---

## 💻 Code Contributions

> **Note**: The source code is currently private. If you're interested in contributing code, please contact the author for access.

### Development Setup

1. **Fork the repository** (if access is granted)
2. **Clone your fork**:
   ```bash
   git clone https://github.com/AndreaBonn/roommate-app.git
   cd roommate-app
   ```

3. **Install dependencies**:
   ```bash
   npm install
   cd frontend && npm install
   cd ../email-service && npm install
   ```

4. **Set up environment variables**:
   - Copy `.env.example` files
   - Fill in your Firebase credentials
   - Configure email service (optional)

5. **Start development servers**:
   ```bash
   # Terminal 1 - Frontend
   cd frontend
   npm run dev

   # Terminal 2 - Email Service (optional)
   cd email-service
   npm start
   ```

### Development Workflow

1. **Create a branch**:
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

2. **Make your changes**:
   - Write clean, readable code
   - Follow the style guidelines
   - Add comments for complex logic
   - Update documentation if needed

3. **Test your changes**:
   - Test manually in the browser
   - Check for console errors
   - Test on different screen sizes
   - Verify offline functionality (if applicable)

4. **Commit your changes**:
   ```bash
   git add .
   git commit -m "feat: add amazing feature"
   ```

5. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Create a Pull Request**

---

## 🎨 Style Guidelines

### TypeScript/JavaScript

- Use **TypeScript** for all new code
- Follow **ESLint** rules (run `npm run lint`)
- Use **functional components** with hooks
- Prefer **const** over let, avoid var
- Use **arrow functions** for callbacks
- Use **async/await** over promises when possible

**Example:**

```typescript
// Good ✅
const MyComponent: React.FC<Props> = ({ title, onSave }) => {
  const [data, setData] = useState<Data | null>(null);

  const handleSave = async () => {
    try {
      await saveData(data);
      onSave();
    } catch (error) {
      console.error('Save failed:', error);
    }
  };

  return <div>{title}</div>;
};

// Bad ❌
function MyComponent(props) {
  var data = null;
  
  function handleSave() {
    saveData(data).then(() => {
      props.onSave();
    }).catch((error) => {
      console.log(error);
    });
  }

  return <div>{props.title}</div>;
}
```

### React Components

- One component per file
- Use meaningful component names (PascalCase)
- Props interface should be defined
- Use destructuring for props
- Keep components small and focused

### CSS/Tailwind

- Use **Tailwind CSS** utility classes
- Avoid custom CSS when possible
- Use responsive classes (sm:, md:, lg:)
- Group related classes together

**Example:**

```tsx
// Good ✅
<button className="px-4 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700 transition-colors">
  Save
</button>

// Avoid ❌
<button className="custom-button" style={{ backgroundColor: 'blue' }}>
  Save
</button>
```

### File Organization

```
src/
├── components/          # Reusable components
│   ├── Button.tsx
│   └── Modal.tsx
├── pages/              # Page components
│   ├── DashboardPage.tsx
│   └── SpesePage.tsx
├── services/           # API and Firebase services
│   ├── casa.service.ts
│   └── spesa.service.ts
├── hooks/              # Custom hooks
│   └── useCasaData.ts
├── types/              # TypeScript types
│   └── index.ts
└── utils/              # Utility functions
    └── helpers.ts
```

---

## 📝 Commit Messages

We follow the [Conventional Commits](https://www.conventionalcommits.org/) specification:

### Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Changes that don't affect code meaning (formatting, etc.)
- **refactor**: Code change that neither fixes a bug nor adds a feature
- **perf**: Performance improvement
- **test**: Adding or updating tests
- **chore**: Changes to build process or auxiliary tools

### Examples

```bash
# Feature
git commit -m "feat(spese): add expense category filter"

# Bug fix
git commit -m "fix(turni): resolve shift rotation calculation error"

# Documentation
git commit -m "docs(readme): update installation instructions"

# Refactoring
git commit -m "refactor(components): extract common modal logic"

# With body
git commit -m "feat(ai): add Groq provider support

- Add Groq API integration
- Update provider selection UI
- Add Groq to fallback chain"
```

---

## 🔄 Pull Request Process

1. **Update documentation** if you've changed APIs or added features
2. **Update the README** if needed
3. **Ensure all tests pass** (when test suite is available)
4. **Update CHANGELOG** (if applicable)
5. **Request review** from maintainers

### Pull Request Template

```markdown
## Description
Brief description of what this PR does.

## Type of Change
- [ ] Bug fix (non-breaking change which fixes an issue)
- [ ] New feature (non-breaking change which adds functionality)
- [ ] Breaking change (fix or feature that would cause existing functionality to not work as expected)
- [ ] Documentation update

## How Has This Been Tested?
Describe the tests you ran and how to reproduce them.

## Checklist
- [ ] My code follows the style guidelines
- [ ] I have performed a self-review
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have tested on multiple browsers/devices

## Screenshots (if applicable)
Add screenshots to help explain your changes.

## Related Issues
Closes #(issue number)
```

---

## 🧪 Testing Guidelines

### Manual Testing Checklist

Before submitting a PR, test:

- [ ] Feature works as expected
- [ ] No console errors
- [ ] Responsive design (mobile, tablet, desktop)
- [ ] Works in Chrome, Firefox, Safari
- [ ] Offline functionality (if applicable)
- [ ] No performance regressions
- [ ] Accessibility (keyboard navigation, screen readers)

### Future: Automated Testing

We plan to add:
- Unit tests (Jest + React Testing Library)
- Integration tests
- E2E tests (Playwright/Cypress)

---

## 📚 Resources

### Documentation

- [React Documentation](https://react.dev/)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Firebase Documentation](https://firebase.google.com/docs)

### Tools

- [VS Code](https://code.visualstudio.com/) - Recommended IDE
- [React Developer Tools](https://react.dev/learn/react-developer-tools)
- [Firebase Emulator Suite](https://firebase.google.com/docs/emulator-suite)

---

## 💬 Communication

- **Issues**: For bug reports and feature requests
- **Email**: andreabonacci95@protonmail.com for private matters
- **Discussions**: (Coming soon) For questions and general discussion

---

## 🏆 Recognition

Contributors will be recognized in:
- README acknowledgments section
- Release notes
- Contributors page (coming soon)

---

## ❓ Questions?

Don't hesitate to ask! You can:
- Open an issue with the "question" label
- Email the maintainer
- Check existing documentation

---

Thank you for contributing to RoomMate App! 🎉

---

# Contribuire (Italiano)

> **🇮🇹 Italiano** | **[🇬🇧 Read in English](#contributing-to-roommate-app)**

---

Prima di tutto, grazie per aver considerato di contribuire a RoomMate App! Sono persone come te che rendono questo progetto migliore.

## 📋 Indice

- [Codice di Condotta](#codice-di-condotta)
- [Come Posso Contribuire?](#come-posso-contribuire)
- [Segnalare Bug](#segnalare-bug)
- [Suggerire Funzionalità](#suggerire-funzionalità)
- [Contributi al Codice](#contributi-al-codice)
- [Linee Guida di Stile](#linee-guida-di-stile)
- [Messaggi di Commit](#messaggi-di-commit)
- [Processo Pull Request](#processo-pull-request)

---

## 📜 Codice di Condotta

Questo progetto e tutti coloro che vi partecipano sono governati dal nostro Codice di Condotta. Partecipando, ci si aspetta che tu rispetti questo codice. Segnala comportamenti inaccettabili a andreabonacci95@protonmail.com.

### I Nostri Standard

**I comportamenti positivi includono:**
- Usare un linguaggio accogliente e inclusivo
- Essere rispettosi di punti di vista ed esperienze diverse
- Accettare con grazia le critiche costruttive
- Concentrarsi su ciò che è meglio per la comunità
- Mostrare empatia verso gli altri membri della comunità

**I comportamenti inaccettabili includono:**
- Trolling, commenti offensivi/denigratori e attacchi personali o politici
- Molestie pubbliche o private
- Pubblicare informazioni private altrui senza permesso esplicito
- Altri comportamenti che potrebbero ragionevolmente essere considerati inappropriati

---

## 🤝 Come Posso Contribuire?

### Segnalare Bug

Prima di creare segnalazioni di bug, controlla le issue esistenti per evitare duplicati. Quando crei una segnalazione di bug, includi quanti più dettagli possibile:

**Template Segnalazione Bug:**

```markdown
**Descrivi il bug**
Una descrizione chiara e concisa di cos'è il bug.

**Per Riprodurre**
Passi per riprodurre il comportamento:
1. Vai a '...'
2. Clicca su '....'
3. Scorri fino a '....'
4. Vedi errore

**Comportamento atteso**
Una descrizione chiara e concisa di cosa ti aspettavi che accadesse.

**Screenshot**
Se applicabile, aggiungi screenshot per aiutare a spiegare il problema.

**Ambiente:**
 - OS: [es. Windows 10, macOS 12, Ubuntu 22.04]
 - Browser: [es. Chrome 120, Firefox 121, Safari 17]
 - Versione App: [es. 1.0.0]
 - Dispositivo: [es. Desktop, iPhone 12, Samsung Galaxy S21]

**Contesto aggiuntivo**
Aggiungi qualsiasi altro contesto sul problema qui.
```

### Suggerire Funzionalità

I suggerimenti di funzionalità sono benvenuti! Prima di creare una richiesta di funzionalità:

1. Controlla se la funzionalità è già stata suggerita
2. Assicurati che sia in linea con gli obiettivi del progetto
3. Fornisci un caso d'uso chiaro

**Template Richiesta Funzionalità:**

```markdown
**La tua richiesta di funzionalità è relativa a un problema?**
Una descrizione chiara e concisa di qual è il problema. Es. Sono sempre frustrato quando [...]

**Descrivi la soluzione che vorresti**
Una descrizione chiara e concisa di cosa vorresti che accadesse.

**Descrivi alternative che hai considerato**
Una descrizione chiara e concisa di eventuali soluzioni o funzionalità alternative che hai considerato.

**Contesto aggiuntivo**
Aggiungi qualsiasi altro contesto o screenshot sulla richiesta di funzionalità qui.

**Vorresti implementare questa funzionalità?**
Facci sapere se sei interessato a lavorarci!
```

---

## 💻 Contributi al Codice

> **Nota**: Il codice sorgente è attualmente privato. Se sei interessato a contribuire con codice, contatta l'autore per l'accesso.

### Setup Sviluppo

1. **Fai il fork del repository** (se l'accesso è concesso)
2. **Clona il tuo fork**:
   ```bash
   git clone https://github.com/AndreaBonn/roommate-app.git
   cd roommate-app
   ```

3. **Installa le dipendenze**:
   ```bash
   npm install
   cd frontend && npm install
   cd ../email-service && npm install
   ```

4. **Configura le variabili d'ambiente**:
   - Copia i file `.env.example`
   - Inserisci le tue credenziali Firebase
   - Configura il servizio email (opzionale)

5. **Avvia i server di sviluppo**:
   ```bash
   # Terminale 1 - Frontend
   cd frontend
   npm run dev

   # Terminale 2 - Servizio Email (opzionale)
   cd email-service
   npm start
   ```

### Workflow di Sviluppo

1. **Crea un branch**:
   ```bash
   git checkout -b feature/nome-tua-funzionalità
   # oppure
   git checkout -b fix/tua-correzione-bug
   ```

2. **Fai le tue modifiche**:
   - Scrivi codice pulito e leggibile
   - Segui le linee guida di stile
   - Aggiungi commenti per logica complessa
   - Aggiorna la documentazione se necessario

3. **Testa le tue modifiche**:
   - Testa manualmente nel browser
   - Controlla errori nella console
   - Testa su diverse dimensioni schermo
   - Verifica funzionalità offline (se applicabile)

4. **Committa le tue modifiche**:
   ```bash
   git add .
   git commit -m "feat: aggiungi funzionalità incredibile"
   ```

5. **Pusha al tuo fork**:
   ```bash
   git push origin feature/nome-tua-funzionalità
   ```

6. **Crea una Pull Request**

---

Per le sezioni rimanenti (Linee Guida di Stile, Messaggi di Commit, ecc.), fare riferimento alla versione inglese sopra, poiché i concetti tecnici sono universali.

---

Grazie per aver contribuito a RoomMate App! 🎉

---

**[🏠 Back to README](./README.md)** | **[🏠 Torna al README](./README_IT.md)**
