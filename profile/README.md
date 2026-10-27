# A Kenyér

Az **A Kenyér** pékség saját fejlesztésű szoftverei és üzemeltetési kódja.

## Projektek

| Repó | Leírás |
| --- | --- |
| **Vekni** | A pékség webes adminisztrációs felülete: számlák, cégek és kategóriák, felhasználók, szerepkörök, rendszerüzenetek. Spring Boot (Java) backend, Angular frontend. |
| **Ansible** | A Veknit kiszolgáló szerver automatizált telepítése és karbantartása. |

A repók privátak, csak a szervezet tagjai látják őket.

## Hogyan dolgozunk

- Minden változás pull requesten keresztül kerül a `main` ágba, és csak zöld CI-jal olvasztjuk be.
- A kódot minden változásnál automatikus tesztek és CodeQL biztonsági elemzés ellenőrzi.
- A függőségeket és a GitHub Actions lépéseit a Dependabot hetente frissíti.
- Az actionök teljes commit SHA-ra vannak rögzítve, és csak a GitHub és a Docker saját actionjei futhatnak.
- A szervezetben kötelező a kétlépcsős azonosítás.

Részletek a [hozzájárulási útmutatóban](https://github.com/AKenyer/.github/blob/main/CONTRIBUTING.md).

## Biztonság

Biztonsági hibát ne nyilvános issue-ban jelezz, hanem [privát bejelentésként](https://github.com/AKenyer/.github/security/advisories/new). Részletek a [biztonsági irányelvekben](https://github.com/AKenyer/.github/blob/main/SECURITY.md).
