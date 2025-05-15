# 📚 Dokumentacja API

## Autoryzacja

Wszystkie endpointy wymagają nagłówka z tokenem JWT:

```
Authorization: Bearer <token>
```

## Endpointy

### 1. `GET /api/uzytkownicy`

Zwraca listę użytkowników.

#### Parametry

| Nazwa      | Typ     | Opis                  | Wymagany |
|------------|---------|-----------------------|----------|
| limit      | int     | Limit wyników         | Nie      |
| offset     | int     | Przesunięcie          | Nie      |

#### Przykład odpowiedzi

```json
[
  {
    "id": 1,
    "imie": "Jan",
    "email": "jan@przyklad.pl"
  }
]
```

---

### 2. `POST /api/zadania`

Tworzy nowe zadanie.

#### Body (JSON)

```json
{
  "nazwa": "Nowe zadanie",
  "opis": "Opis zadania"
}
```

#### Przykład odpowiedzi

```json
{
  "id": 101,
  "nazwa": "Nowe zadanie",
  "status": "utworzone"
}
```

---

## Błędy

| Kod | Znaczenie      |
|-----|---------------|
| 401 | Unauthorized  |
| 404 | Not found     |
| 500 | Server error  |

---

*Więcej endpointów wkrótce!*
