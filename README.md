# Wyjazd do USA — strona rodzinna

Statyczna strona (trzy pliki HTML, bez zależności) gotowa pod GitHub Pages.

## Publikacja

1. Utwórz repozytorium, np. `usa-2026`.
2. Wrzuć zawartość tego folderu do gałęzi `main`.
3. Settings → Pages → Source: *Deploy from a branch*, Branch: `main` / `/ (root)`.
4. Po chwili strona działa pod `https://<nazwa-konta>.github.io/usa-2026/`.

Plik `.nojekyll` wyłącza przetwarzanie Jekyllem — bez niego GitHub potrafi pomijać
niektóre pliki. Nie kasuj go.

## Własna domena

Settings → Pages → Custom domain. W DNS dodaj rekord CNAME wskazujący na
`<nazwa-konta>.github.io`. Poczekaj na wystawienie certyfikatu, potem zaznacz
*Enforce HTTPS*.

## Pliki

| plik         | co to                                                        |
|--------------|--------------------------------------------------------------|
| `index.html` | strona dla rodziny: plan, mapa, pakowanie, budżet, notatki   |
| `mapa.html`  | mapa drogowa z linkami do Google Maps dla każdego odcinka    |
| `plan.html`  | szczegóły logistyczne: loty, opłaty, auto, plan awaryjny     |

## Notatki

Notatki i odhaczona lista pakowania zapisują się w `localStorage`, czyli
w przeglądarce każdej osoby osobno. Nikt nie widzi cudzych wpisów — dlatego pod
notatkami jest przycisk kopiujący wszystko do schowka.

Żeby notatki były wspólne i widoczne dla wszystkich, trzeba podpiąć backend
(np. darmowy projekt w Supabase). Strona jest przygotowana tak, że wymaga to
podmiany jednej funkcji w sekcji `/* ---- notes ---- */` w `index.html`.

## Dane

Przebieg dróg: OpenStreetMap (przez OSRM). Granice stanów: US Census.
Parki: Natural Earth + National Park Service. Stan na wrzesień 2026.
