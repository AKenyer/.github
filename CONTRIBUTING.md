# Hozzájárulási útmutató

Ez az útmutató az AKenyer szervezet minden repójára vonatkozik, hacsak a repó saját `CONTRIBUTING.md` fájlja mást nem mond.

## Munkafolyamat

1. Ágazz le a friss `main`-ről. Az ág neve utaljon a változásra, például `feat/szamla-export`, `fix/login-lockout`, `ci/codeql`, `docs/readme`.
2. Kis, egy témára szorítkozó commitokat készíts.
3. Nyiss pull requestet a `main` felé, és töltsd ki a sablont.
4. A CI-nak és a CodeQL-nek zöldnek kell lennie. Piros ellenőrzéssel nem olvasztunk be.
5. Beolvasztás után az ág automatikusan törlődik.

A `main` ágra közvetlenül nem pusholunk, és a történetét nem írjuk át (nincs force push).

## Commitok

- Az összefoglaló sor angol, felszólító módú, és legfeljebb nagyjából 72 karakter: `Add invoice export`, `Fix lockout for IPv6 clients`.
- Ha kell, egy üres sor után írd le, *miért* változott valami.

## Kód és dokumentáció

- A kód és a commitok angolul, a felhasználói felület és a dokumentáció magyarul készül.
- Tartsd be a repó saját szabályait (formázás, tesztek, `CLAUDE.md`). A formázást a CI ellenőrzi.
- Új funkcióhoz és hibajavításhoz tartozzon teszt.

## GitHub Actions

- Csak `actions/*`, `github/*` és `docker/*` actionök futhatnak, minden mást a szervezet blokkol.
- Minden actiont teljes commit SHA-ra rögzíts, a verziót pedig írd mögé kommentben:
  `uses: actions/checkout@11d5960a326750d5838078e36cf38b85af677262 # v4.4.0`
- A workflow-k tokenje alapból csak olvasni tud. Csak azt a jogosultságot kérd, amire tényleg szükség van.
- A Dependabot frissítéseit ugyanúgy nézd át, mint bármely más pull requestet.

## Titkok

Jelszó, token, kulcs, `.env` vagy titkosítatlan `vault.yml` soha nem kerülhet a repóba. A titkok helye a GitHub Secrets, illetve titkosítva az Ansible Vault. Ha mégis bekerült valami, azonnal cseréld le a titkot: a git történetből való törlés önmagában nem elég.

## Biztonsági hibák

Lásd a [biztonsági irányelveket](SECURITY.md).
