# Plan Projektu — Interaktywna Mapa Gothic II

## 1. Architektura projektu

### 1.1. SPA (Single Page Application)
- Jednostronicowa aplikacja z dynamicznym przełączaniem widoków.
- Renderowanie mapy i paneli informacyjnych bez przeładowania strony.

### 1.2. Monolit
- Frontend i backend w jednym repozytorium.
- Backend obsługuje API, autoryzację i zapis danych.

### 1.3. Mikroserwisy (opcjonalnie)
- Serwis mapowy (tiles, warstwy).
- Serwis danych (lokacje, NPC, questy).
- Serwis autoryzacji (tokeny API).

### 1.4. REST API
- `GET /locations`
- `GET /locations/:id`
- `GET /npcs`
- `GET /quests`
- `POST /locations`
- `GET /map/tiles`
- `POST /auth/token`

### 1.5. SSR (opcjonalnie)
- Możliwe użycie Vite SSR lub Astro.
- Przydatne dla SEO i szybszego pierwszego renderu.

### 1.6. MVC
- **Model:** dane o lokacjach, NPC, questach  
- **View:** mapa + UI  
- **Controller:** obsługa interakcji użytkownika  

---

## 2. Stos technologiczny

### 2.1. Języki
- JavaScript
- PHP
- HTML, CSS
- JSON
- Markdown

### 2.2. Frameworki i biblioteki

#### Frontend
- Vite
- Leaflet.js lub MapLibre
- marked.js
- Vanilla JS lub Svelte/React (opcjonalnie)

#### Backend
- PHP 8.x
- Slim Framework lub czysty PHP

### 2.3. Narzędzia
- Visual studio code
- GitHub

---

## 3. Przykładowe funkcjonalności i przepływy UX/UI

### 3.1. Widok główny
- Interaktywna mapa z warstwami.
- Panel boczny z filtrami.
- Wyszukiwarka lokacji/NPC.

### 3.2. Interakcje użytkownika
- Hover: nazwa lokacji.
- Klik: panel szczegółów (opis, screenshot, powiązane questy).
- Zoom: zmiana poziomu szczegółowości.

### 3.3. Przepływ danych
1. Użytkownik otwiera stronę.  
2. Frontend pobiera `/map/tiles` i `/locations`.  
3. Renderuje warstwy mapy.  
4. Kliknięcie → zapytanie do `/locations/:id`.  
5. Wyświetlenie danych w panelu.  

---

## 4. Grupa docelowa

### 4.1. Odbiorcy
- Fani Gothic II
- Modderzy
- Twórcy poradników
- Speedrunnerzy
- Nowi gracze

### 4.2. Potrzeby
- Dokładna mapa świata
- Informacje o NPC, potworach, lokacjach
- Filtrowanie i wyszukiwanie
- Wersja mobilna

---

## 4. Wymagania techniczne
- Hosting statyczny + backend PHP
- API zabezpieczone tokenami
- Responsywność (mobile-first)
- Lazy loading tiles
- Cache danych (localStorage)

---

## 5. Standaryzacja

### 5.1. WCAG 2.1
- Kontrast
- Opisy alternatywne
- Obsługa klawiaturą

### 5.2. SEO
- SSR lub prerendering
- Metadane dla mapy i lokacji
  - Sitemap

---
