---
title: Kirjanpito- tai raportointivaluutan muuttaminen
description: Tässä artikkelissa kerrotaan, miten kirjanpito- tai raportointivaluutta vaihdetaan tai miten raportointivaluutta lisätään kirjanpidon asetuksiin.
author: kweekley
ms.date: 05/05/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-05-05
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b02432c8e0bdf52c2a588f67a581b78e682b1bf8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904611"
---
# <a name="change-the-accounting-or-reporting-currency"></a>Kirjanpito- tai raportointivaluutan muuttaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten kirjanpito- tai raportointivaluutta vaihdetaan tai miten raportointivaluutta lisätään kirjanpidon asetuksiin.

## <a name="symptom"></a>Oire

Haluat vaihtaa kirjanpito- tai raportointivaluutan tai lisätä raportointivaluutan kirjanpidon asetuksiin. Tämä tapahtuu yleensä seuraavissa tilanteissa:

- Yrityksen määrityksen yhteydessä määritettiin väärä kirjanpito- tai raportointivaluutta. Haluat muuttaa tämän valuutan nyt.
- Raportointivaluutta määritettiin yrityksen määrityksen yhteydessä, mutta organisaatio haluaa nyt poistaa raportointivaluutan.
- Organisaatio päivittää Microsoft Dynamics 365 Financen tai siirtyy käyttämään sitä ja haluaa muuttaa kirjanpito- tai raportointivaluutan.

Organisaatio, joka ei aiemmin käyttänyt kaksoisvaluuttaominaisuutta, haluaa nyt alkaa käyttää sitä. Tämä virhe tapahtuu yleensä seuraavissa tilanteissa.

- Yrityksen määrityksen yhteydessä ei määritetty raportointivaluuttaa. (Raportointivaluutta on valinnainen.) Haluat nyt lisätä raportointivaluutan.

## <a name="resolution"></a>Ratkaisu

Tärkeintä on ottaa huomioon, onko yrityksessä kirjattu kirjanpidon asetuksiin tapahtumia (todellisia tai budjetoituja). **Et voi muuttaa kirjanpito- tai raportointivaluuttaa tai lisätä raportointivaluuttaa, jos yrityksessä on kirjattu tapahtumia (todellisia tai budjetoituja).** Noudata jonkin seuraavan osan vaiheita sen mukaan, mitä tapahtumia on kirjattu.

### <a name="no-transactions-have-been-posted"></a>Tapahtumia ei ole kirjattu

1. Siirry kohtaan **Kirjanpito \> Kirjanpidon asetukset \> Kirjanpito** siinä yrityksessä, jonka valuuttoja päivitetään.
2. Valitse **Kirjanpito**-sivulla **Muokkaa**.
3. Valitse **Valuutta**-pikavälilehdessä yrityksessä käytettävä kirjanpito- ja raportointivaluutta.
4. Valitse **Tallenna**.

Jos kirjanpito- ja raportointivaluutan kentät eivät ole käytettävissä **Kirjanpito**-sivulla, yrityksessä on kirjattu vähintään yksi tapahtuma (todellinen tai budjetoitu). Tämän vuoksi valuuttoja ei voi muuttaa. Noudata tässä tapauksessa seuraavan osan ohjeita.

### <a name="transactions-have-been-posted"></a>Tapahtumia on kirjattu

**Jos yrityksessä on kirjattu tapahtumia, ainoa mahdollinen tapa muuttaa kirjanpito- tai raportointivaluuttoja tai lisätä niitä on luoda uusi yritys, jolla on oikeat valuutat.** Tätä prosessia helpottaa järjestelmän tietojen hallinta, jonka avulla voit kopioida asetustietueita ja päätietueita nykyisestä yrityksestä uuteen yritykseen.

Kirjanpito- ja raportointivaluuttojen muutokset tehdään kaikkialla. Ne vaikuttavat sekä kirjanpitoon että jokaiseen alikirjanpitoon (esimerkiksi myyntireskontra, ostoreskontra, varasto ja projekti), jokaiseen riippumattoman ohjelmistotoimittajan ratkaisuun ja mahdollisiin summia sisältäviin laajennuksiin.

Kunkin summan etsintäprosessi ja muuntaminen eri valuutaksi voi sisältää virheitä. Tämän vuoksi kehitysryhmä ei hyväksy skriptiä, joka muuttaa kirjanpito- tai raportointivaluuttoja tai lisää niitä. Microsoft Dynamics AX 2012:n työkalun avulla oli mahdollista muuttaa kirjanpito- ja raportointivaluuttoja ja lisätä niitä. Tämä työkalu vanhentui sekä AX 2012 R3:ssa että Financessa.

Näiden ohjeiden avulla voit kopioida asetukset ja päätiedot nykyisestä yrityksestä uuteen yritykseen.

1. Valitse **Työtilat \> Tietojen hallinta**.
2. Valitse **Mallit** **Tuonti/vienti**-ryhmässä.
3. Varmista, että mallit ovat käytettävissä. Jos malleja ei ole käytettävissä, valitse **Lataa oletusmallit** ja odota, kunnes mallit on luotu.
4. Palaa **Tietojen hallinta** -työtilaan.
5. Valitse **Kopioi yritykseen**.
6. Syötä ryhmän nimi ja kuvaus.
7. Valitse **Lähdeyritys**-kentässä yritys, josta tiedot kopioidaan.
8. Valitse **Kohdeyritykset**-pikavälilehdessä **Luo yritykset**, jos haluat luoda uuden yrityksen, johon lähdeyrityksen tiedot kopioidaan. Valitse **Valitse olemassa oleva**, jos haluat kopioida tietoja olemassa olevaan yritykseen.
9. Valinnainen: Määritä **Kopioi numerosarjat** -kentän arvoksi **Kyllä**. (Tätä vaihetta suositellaan tietojen kopioimisen yhteydessä.)
10. Valitse **Valitut entiteetit** -alueessa **Lisää malli**.
11. Valitse käytettävät mallit. Uudelle yritykselle ehdotettuja malleja ovat **025 - Kirjanpito** ja **Taloushallinto**. Myös muut käytettävissä olevat mallit kannattaa käydä läpi. Tämän jälkeen voit määrittää, vastaako jokin niistä vaatimuksiasi.
12. Valitse **Kopioi yritykseen**, jotta voit aloittaa eräprosessin, luoda valitut yksiköt ja kopioida ne kohdeyritykseen.
13. Kun prosessi on valmis, mutta tapahtumia ei ole vielä kirjattu, siirry kirjanpitoon ja päivitä kirjanpito- ja raportointivaluutat aiemmin tässä artikkelissa kuvatulla tavalla.

Jos olet luonut uuden yrityksen niin, että muutat kirjanpito- tai raportointivaluuttaa, varmista, että alkusaldot on muutettu vanhan yrityksen valuutoista uuden yrityksen valuutoiksi.

Lisätietoja edellisistä vaiheista on videossa [Kopioiminen yritykseen](https://community.dynamics.com/365/b/techtalks/posts/copy-into-legal-entity-october-24-2017).
