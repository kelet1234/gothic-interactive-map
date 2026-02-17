Jasne — przygotuję **ten sam plan**, ale w czystej, poprawnej **formie Markdown**, bez komentarzy, bez dodatkowych opisów.  
Poniżej masz gotowy plik `.md`, który możesz wkleić bezpośrednio do repozytorium.

---

```markdown
# 📌 Plan Projektu — Interaktywna Mapa Gothic II

## 1. Tytuł roboczy / nazwa kodowa
- **G2 Interactive Atlas**
- **Atlas Khorinis**

---

## 2. Architektura projektu

### 2.1. SPA (Single Page Application)
- Jednostronicowa aplikacja z dynamicznym przełączaniem widoków.
- Renderowanie mapy i paneli informacyjnych bez przeładowania strony.

### 2.2. Monolit
- Frontend i backend w jednym repozytorium.
- Backend obsługuje API, autoryzację i zapis danych.

### 2.3. Mikroserwisy (opcjonalnie)
- Serwis mapowy (tiles, warstwy).
- Serwis danych (lokacje, NPC, questy).
- Serwis autoryzacji (tokeny API).

### 2.4. REST API
- `GET /locations`
- `GET /locations/:id`
- `GET /npcs`
- `GET /quests`
- `POST /locations`
- `GET /map/tiles`
- `POST /auth/token`

### 2.5. SSR (opcjonalnie)
- Możliwe użycie Vite SSR lub Astro.
- Przydatne dla SEO i szybszego pierwszego renderu.

### 2.6. MVC
- **Model:** dane o lokacjach, NPC, questach  
- **View:** mapa + UI  
- **Controller:** obsługa interakcji użytkownika  

---

## 3. Stos technologiczny

### 3.1. Języki
- JavaScript
- PHP
- HTML, CSS
- JSON
- Markdown

### 3.2. Frameworki i biblioteki

#### Frontend
- Vite
- Leaflet.js lub MapLibre
- marked.js
- Vanilla JS lub Svelte/React (opcjonalnie)

#### Backend
- PHP 8.x
- Slim Framework lub czysty PHP

### 3.3. Narzędzia
- Node.js
- GitHub (repo + API tokens)
- Tokeny API do autoryzacji i edycji danych

---

## 4. Logika biznesowa

### 4.1. Główne założenia
- Interaktywna mapa Gothic II (Khorinis, Górnicza Dolina, Jarkendar).
- Kliknięcie w punkt otwiera panel z informacjami.
- Dane pobierane z API w formacie JSON.
- Filtry: NPC, potwory, lokacje, złoża rudy, skrzynie, questy.

### 4.2. Uprawnienia
- **Tryb publiczny:** przeglądanie.
- **Tryb edytora:** dodawanie i edycja punktów (token).

---

## 5. Przykładowe funkcjonalności i przepływy UX/UI

### 5.1. Widok główny
- Interaktywna mapa z warstwami.
- Panel boczny z filtrami.
- Wyszukiwarka lokacji/NPC.

### 5.2. Interakcje użytkownika
- Hover: nazwa lokacji.
- Klik: panel szczegółów (opis, screenshot, powiązane questy).
- Zoom: zmiana poziomu szczegółowości.

### 5.3. Przepływ danych
1. Użytkownik otwiera stronę.  
2. Frontend pobiera `/map/tiles` i `/locations`.  
3. Renderuje warstwy mapy.  
4. Kliknięcie → zapytanie do `/locations/:id`.  
5. Wyświetlenie danych w panelu.  

### 5.4. Tryb edytora
- Formularz dodawania punktu:
  - nazwa  
  - typ  
  - opis (markdown)  
  - współrzędne  
- Zapis → `POST /locations`

---

## 6. Grupa docelowa

### 6.1. Odbiorcy
- Fani Gothic II
- Modderzy
- Twórcy poradników
- Speedrunnerzy
- Nowi gracze

### 6.2. Potrzeby
- Dokładna mapa świata
- Informacje o NPC, potworach, lokacjach
- Filtrowanie i wyszukiwanie
- Wersja mobilna

---

## 7. Wymagania techniczne
- Hosting statyczny + backend PHP
- API zabezpieczone tokenami
- Responsywność (mobile-first)
- Lazy loading tiles
- Cache danych (localStorage)

---

## 8. Wymagania prawne

### 8.1. Prawa autorskie
- Brak użycia oryginalnych assetów Gothic II bez licencji.
- Można używać własnych tilesetów i opisów.

### 8.2. RODO / cookies
- Tylko cookies techniczne.
- Brak danych osobowych użytkowników.
- Polityka prywatności w markdown.

### 8.3. Licencje
- Kod: MIT lub GPL
- Dane mapy: CC-BY-SA (jeśli własne)

---

## 9. Standaryzacja

### 9.1. WCAG 2.1
- Kontrast
- Opisy alternatywne
- Obsługa klawiaturą

### 9.2. SEO
- SSR lub prerendering
- Metadane dla mapy i lokacji
- Sitemap

---

## 10. Wymagania końcowe projektu

### 10.1. Dokumentacja techniczna
- JSDoc (frontend)
- PHPDoc (backend)

### 10.2. Dokumentacja logiki biznesowej
- `ARCHITEKTURA.md`
- `API.md`
- `DATA_MODELS.md`
- `UX_FLOW.md`
- `MAP_FEATURES.md`

```

---

Jeśli chcesz, mogę przygotować **kolejne pliki `.md`** z tego planu — np. pełną dokumentację API, modele danych JSON, strukturę repozytorium albo roadmapę.