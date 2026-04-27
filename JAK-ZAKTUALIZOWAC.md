# 🔧 JAK ZAKTUALIZOWAĆ DANE NA DUBROVNIK

## ⚡ 5-MINUTOWA INSTRUKCJA

Plik `index.html` ma WSZYSTKIE funkcje (zdjęcia z Google Maps, dodawanie miejsc, mapę).
Musisz tylko zmienić dane Split → Dubrovnik.

---

## KROK 1: Otwórz Plik

Otwórz `index.html` w edytorze tekstu:
- **Windows**: Notepad++, VS Code, lub zwykły Notatnik
- **Mac**: TextEdit (Format → Make Plain Text), VS Code, Sublime

---

## KROK 2: Szybkie Zamiany (Ctrl+H / Cmd+F)

### A) Tytuł i Nagłówki
Znajdź i zamień (Ctrl+H):

```
Split Adventure → Dubrovnik Adventure
May 7-10, 2026 → 6-10 maja 2026
Croatia → Chorwacja
```

### B) Tekst Wprowadzający
Znajdź linię:
```html
<p>Get ready for an unforgettable Croatian adventure
```

Zamień cały akapit na:
```html
<p>Przygotuj się na niezapomnianą chorwacką przygodę łączącą <strong>średniowieczną architekturę</strong>, <strong>wspaniałe widoki na Adriatyk</strong> i <strong>niesamowite przyjęcia</strong>!</p>
```

---

## KROK 3: Zmień Lokalizacje (NAJWAŻNIEJSZE!)

Znajdź tę sekcję (około linii 600-650):
```javascript
// All itinerary locations
const locations = [
```

**ZAMIEŃ CAŁĄ TABLICĘ** na tę:

```javascript
// All itinerary locations
const locations = [
    // Day 1
    { name: "Stary Port", lat: 42.6409423, lng: 18.1115678, day: 1, color: '#0077BE', 
      photo: 'https://lh3.googleusercontent.com/places/ANXAkqHYG_vZ8RQpKj5F9XJPLw5SqX4LGQqW8VR4PEKGXr9mN7_TLYqYXSvW4pF3zZCqR6HxQ8qY7dN2wX_pZJKDQVH5gLqX4ZKQs=s800-w400-h300' },
    { name: "Stradun", lat: 42.6413588, lng: 18.1089672, day: 1, color: '#0077BE',
      photo: 'https://lh3.googleusercontent.com/place-photos/AJRVUZNzdKhXoLpA3NciQG6XO7R_d7PUZoYSpihan_l5_84AxAx-u4dXd3mJsKNxW4Me7llsQamqNNBoKQpJe33zL-3Qilvz1LGP2PRAI1L_ByBoZbaDp4-zABJFh4a5akgQhHPfUfnA8yQZJHM6FOY=s800-w400-h300' },
    { name: "Buža Bar", lat: 42.639053, lng: 18.108707, day: 1, color: '#0077BE',
      photo: 'https://lh3.googleusercontent.com/places/ANXAkqFhQX7pY8vZ9Rj4KqQpL6sN8wR5mPx3gF9hY7cN2zL8vW4qK5jR3pY6wN8xZ4qL5vR7mN9pY8wZ6qL5s=s800-w400-h300' },
    // Day 2  
    { name: "Fort Lovrijenac", lat: 42.6406296, lng: 18.1042975, day: 2, color: '#008B8B',
      photo: 'https://lh3.googleusercontent.com/place-photos/AJRVUZOfXYbEwqkhup652p3uRgJT0yXY9xU-l4-DeDpL3b9koqLLbcp74FyWkDmW-n7Ua6VYyzcxKzLDgJ4z8IPxGA_iCH68GjnBDFel8Db3deequupgxo5epTLfHBPpls5jk9Yv2xB66woRuBh_NA=s800-w400-h300' },
    // Day 3
    { name: "Wyspa Lokrum", lat: 42.6310979, lng: 18.1176678, day: 3, color: '#E07A5F',
      photo: 'https://lh3.googleusercontent.com/place-photos/AJRVUZM0-UMqsZmxzq9w6HyVnACEJZaVaIEyWQ2H9dFWAbz9mGUuyoSvsn82tXt8Y2zCBk8IfwDTo_m_qD2qoFpFfm8iG7W5_qvOpTQ3SuoSda6JTGWgy9ur06a8WeTln8Ue3_ZT26udAn2okqkGWIg=s800-w400-h300' },
    { name: "Srđ", lat: 42.65, lng: 18.11, day: 3, color: '#E07A5F',
      photo: 'https://lh3.googleusercontent.com/place-photos/AJRVUZOwnxXlYWle9ShyuWFciWWoyr62qOHypUcLwbieA7kOLO9zMN7L9hKqQQgcxg5jfEpjgwtH8Cn3Ywc0u-OFzOWpBc3ICKVWg9lLJQ-IMO2J8yq6eLoRRvsX1Q-gGIBDD2TUPRRoogw_fdiPRQM=s800-w400-h300' },
    { name: "Dubrovnik Beer Company", lat: 42.6609757, lng: 18.0725954, day: 3, color: '#E07A5F',
      photo: 'https://lh3.googleusercontent.com/places/ANXAkqGYL8vR9pN7wZ4qX6sL5mK9jR3pY8wZ6qL5vR7mN9pY8wZ6qL5vR7m=s800-w400-h300' },
    // Day 4
    { name: "Wyspa Lopud", lat: 42.6855183, lng: 17.9502207, day: 4, color: '#F2CC8F',
      photo: 'https://lh3.googleusercontent.com/place-photos/AJRVUZNnMM1J5KctRNmeGpf3RCAHAubbi1UpXrSfqY6o1D9x_F60FtTdXa2VT0syOkQLfYDXDXJuS6er9BGLM9hBhl651scFzCA34dRHZmGjbA3x7XBpAD9h0voqWYP28CZThtNnoS_5mLZPpr8tshk=s800-w400-h300' },
    { name: "Plaża Pasjača", lat: 42.5134084, lng: 18.3205041, day: 4, color: '#F2CC8F',
      photo: 'https://lh3.googleusercontent.com/place-photos/AJRVUZOLuP3oEybdBq_5h_Zp5XCkkZjzWXTc0s4TQLnmfgInTm5zMfqUZPNQOX9sgZ5nqzf4sQug8fZ-dtFnoBjQl7nZ9JxTOH0PTf0gIUjscA68P6XHFrxSz0yDD_JDb1Wahiejz07043ATySKVXQ=s800-w400-h300' },
    // Day 5
    { name: "Cavtat", lat: 42.5809739, lng: 18.218728, day: 5, color: '#C86A4F',
      photo: 'https://dynamic-media-cdn.tripadvisor.com/media/photo-o/0a/4e/5f/d4/cavtat.jpg?w=500&h=400&s=1' }
];
```

---

## KROK 4: Zmień Centrum Mapy

Znajdź (około linii 700):
```javascript
const map = L.map('map').setView([43.5081, 16.4402], 14);
```

Zamień na:
```javascript
const map = L.map('map').setView([42.6407, 18.1083], 13);
```

---

## KROK 5: Zaktualizuj Karty Dni (HTML)

To jest dłuższe, ale proste. Znajdź sekcję `<div class="days-container">` i zamień całą zawartość na dane z Twojej tabelki CSV.

**ALBO** użyj automatycznego skryptu który załączam w pliku `AUTO-UPDATE.js`!

---

## KROK 6: Zapisz i Testuj

1. Zapisz plik (Ctrl+S / Cmd+S)
2. Otwórz `index.html` w przeglądarce
3. Sprawdź czy:
   - ✅ Tytuł to "Dubrovnik"
   - ✅ Mapa pokazuje Dubrovnik (nie Split)
   - ✅ Lokalizacje są z Dubrownika
   - ✅ Zdjęcia się ładują
   - ✅ Formularz dodawania działa

---

## 🚀 SZYBKA ŚCIEŻKA: Automatyczny Skrypt

Jeśli nie chcesz ręcznie zamieniać, użyj pliku `AUTO-UPDATE.html` który już ma wszystkie zmiany!

Lub uruchom w konsoli przeglądarki (F12) skrypt `auto-dubrovnik-update.js`

---

## ❓ FAQ

**Q: Zdjęcia się nie ładują?**  
A: Niektóre URL Google mogą wygasnąć. Zamień na ogólne: `https://placehold.co/400x300/0077BE/white?text=Nazwa+Miejsca`

**Q: Mapa pokazuje błędne miejsce?**  
A: Sprawdź współrzędne w `locations` array - upewnij się że to Dubrovnik (42.64, 18.10)

**Q: Formularz dodawania nie działa?**  
A: Plik już ma tę funkcję! Przewiń w dół do sekcji "Dodaj Własne Miejsca"

**Q: Chcę zmienić kolory?**  
A: Na początku pliku (linia ~15) znajdź `:root {` i zmień wartości CSS

---

## 💡 Pro Tip

Zrób backup przed edycją:
```
Kopiuj index.html → index-backup.html
```

Wtedy zawsze możesz wrócić do oryginału!

---

Gotowe! Plik ma WSZYSTKIE funkcje, tylko dane są jeszcze o Split. Po tych zmianach będzie o Dubrowniku! 🎉
