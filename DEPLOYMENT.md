# 🚀 Instrukcja Wdrożenia na GitHub

## Krok 1: Utwórz Repozytorium GitHub

1. Przejdź do [GitHub.com](https://github.com) i zaloguj się
2. Kliknij ikonę **"+"** w prawym górnym rogu → **"New repository"**
3. Wypełnij:
   - **Nazwa repozytorium**: `dubrovnik-trip` (lub dowolna nazwa)
   - **Opis**: "Interaktywny plan wycieczki do Dubrownika, Chorwacja 🇭🇷"
   - **Public** (wymagane dla darmowego GitHub Pages)
   - **NIE** inicjalizuj z README (już go masz)
4. Kliknij **"Create repository"**

## Krok 2: Wgraj Swoje Pliki

### Opcja A: Przez Przeglądarkę (Najłatwiejsza)

1. Po utworzeniu repozytorium zobaczysz stronę z instrukcjami
2. Poszukaj linku **"uploading an existing file"** (w środkowej sekcji)
3. Kliknij go
4. **Przeciągnij wszystkie pliki** z rozpakowanego folderu:
   - index.html
   - README.md
   - LICENSE
   - DEPLOYMENT.md
   - QUICKSTART.md
   - .gitignore
5. Przewiń w dół i kliknij **"Commit changes"**

### Opcja B: Przez Linię Poleceń (Dla Zaawansowanych)

```bash
cd ścieżka/do/dubrovnik-repo
git init
git add .
git commit -m "Pierwszy commit: Plan wycieczki do Dubrownika"
git branch -M main
git remote add origin https://github.com/TWOJA_NAZWA/dubrovnik-trip.git
git push -u origin main
```

## Krok 3: Włącz GitHub Pages

1. Przejdź do swojego repozytorium na GitHub
2. Kliknij zakładkę **"Settings"**
3. Przewiń w dół do **"Pages"** w lewym menu bocznym
4. W sekcji **"Source"** wybierz:
   - Branch: **main**
   - Folder: **/ (root)**
5. Kliknij **"Save"**

## Krok 4: Zaczekaj i Wejdź na Swoją Stronę

- GitHub Pages zbuduje Twoją stronę (zajmuje 1-2 minuty)
- Twoja strona będzie dostępna pod: `https://TWOJA_NAZWA.github.io/dubrovnik-trip/`
- Dokładny URL znajdziesz w ustawieniach Pages

## 🎉 Gotowe!

Twój plan wycieczki do Dubrownika jest teraz dostępny online!

### Udostępnij Znajomym:
Wyślij im link GitHub Pages. Mogą:
- Przeglądać interaktywną mapę
- Klikać lokalizacje aby otworzyć w Google Maps
- Przeglądać na telefonie podczas wycieczki

## 📱 Dodatkowe Wskazówki

### Problem: Strona nie działa
- Sprawdź czy w Settings → Pages jest zielony komunikat "Your site is published at..."
- Poczekaj 2-3 minuty i odśwież
- Upewnij się, że branch to "main" a folder to "/ (root)"

### Problem: Nie widzę "uploading an existing file"
- To pojawia się tylko gdy repozytorium jest puste
- Jeśli już dodałeś pliki, użyj: **"Add file"** → **"Upload files"** (przycisk w prawym górnym rogu)

## 🔄 Przyszłe Aktualizacje

Kiedy wprowadzisz zmiany w pliku:

### Przez Przeglądarkę:
1. Otwórz repozytorium na GitHub
2. Kliknij na plik do edycji
3. Kliknij ikonę ołówka (Edit)
4. Wprowadź zmiany
5. Przewiń w dół → "Commit changes"

### Przez Linię Poleceń:
```bash
git add .
git commit -m "Opis zmian"
git push
```

GitHub Pages automatycznie zaktualizuje Twoją stronę!

---

**Potrzebujesz Pomocy?** Sprawdź [Dokumentację GitHub Pages](https://docs.github.com/en/pages)
