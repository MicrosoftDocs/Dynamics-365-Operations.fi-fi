---
title: Verolaskelma-apuohjelman käytön aloittaminen
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää verolaskelma-apuohjelman.
author: wangchen
ms.date: 03/10/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 835ae33fba31d4bccb218969aa9aa61eaa7a3061
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832590"
---
# <a name="get-started-with-the-tax-calculation-add-in-preview"></a>Verolaskelma-apuohjelman käytön aloittaminen (esiversio)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja verolaskelma-apuohjelman käytön aloittamisesta. Ensin se opastaa sinua Microsoft Dynamics Lifecycle Servicesin (LCS), Regulatory Configuration Servicen (RCS) ja Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin määritysvaiheissa. Tämän jälkeen se tarkastelee yleistä prosessia, jossa veronlaskenta-apuohjelmaa käytetään Financen ja Supply Chain Managementin tapahtumissa.

Asetukset koostuvat neljästä päävaihesta:

1. Asenna LCS:ssä verolaskelma-apuohjelma.
2. Määritä RCS:ssä veronlaskentaominaisuus. Nämä määritykset eivät ole yrityskohtaisia. Se voidaan jakaa Financen ja Supply Chain Managementin oikeushenkilöiden kanssa.
3. Määritä Financessa ja Supply Chain Managementissa verolaskelma-apuohjelman parametrit oikeushenkilöittäin.
4. Luo Financessa ja Supply Chain Managementissa tapahtumia, kuten myyntitilauksia, ja määritä ja laske verot verolaskelma-apuohjelman avulla.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Voit käyttää LCS-tiliäsi ja olet ottanut käyttöön LCS-projektin, jossa on taso 2 (tai korkeampi) ympäristö, jossa on Dynamics 365:n versio 10.0.18 tai uudempi.
- Sinull on pääsy RCS-tiliisi.
- Olet ottanut yhteyttä Microsoftiin ottaaksesi väliversiot käyttöön ottamassasi Finance- tai Supply Chain Management -ympäristössä.

## <a name="set-up-the-tax-calculation-add-in-in-lcs"></a>Määrtä LCS:ssä verolaskelma-apuohjelma

1. Kirjaudu [LCS-palveluun](https://lcs.dynamics.com)
2. Viimeistele Microsoft Power Platform -integroinnin asetukset. Lisätietoja on kohdassa [Apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Valitse jokin käyttöön otettu muu kuin tuotantoympäristö ja valitse sitten **Asenna uusi apuohjelma**.
4. Valitse **Verolaskelma (esiversio)**.
5. Lue ja hyväksy käyttöehdot ja valitse sitten **Asenna**.

## <a name="set-up-the-tax-calculation-add-in-in-rcs"></a>Määrtä RCS:ssä verolaskelma-apuohjelma

Tämän osan vaiheet eivät liity tiettyyn oikeushenkilöön. Sinun on suoritettava tämä toiminto vain kerran, ja voit suorittaa sen missä tahansa RCS:n oikeushenkilössä.

1. Kirjaudu sisään [RCS:ään](https://marketing.configure.global.dynamics.com/).
2. Valitse Financessa **Sähköinen raportointi** -työtila, lisää uusi määrityspalvelu. Käytä yrityksesi nimeä palveluntarjoajan nimenä. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Valitse juuri luomasi määrityspalvelu ja valitse sitten **Aseta aktiiviseksi**.
4. Valitse **Microsoft**-määrityspalvelu ja valitse sitten **Säilöt**.
5. Kirjoita **Tyyppi**-kenttään **Yleinen**.
6. Valitse **Avaa**.
7. Siirry kohtaan **Verotietomalli**, laajenna tiedostopuu ja valitse sitten **Veromääritys – Eurooppa**.
8. Valitse uusin versio ja valitse sitten **Tuo**.
9. Palaa **Globalisaatio-ominaisuudet (esiversio)** -työtilaan, valitse **Ominaisuudet**, valitse **Verolaskelma**-ruutu ja valitse sitten **Lisää**.
10. Valitse jokin seuraavista ominaisuustyypeistä:

    - **Uusi ominaisuus** – Luo ominaisuusasetus, jonka sisältö on tyhjä.
    - **Aiemmin luodun ominaisuuden perusteella** – Luo ominaisuus aiemmin luodusta ominaisuudesta ja kopioi sisältö aiemmin luoduista ominaisuusasetuksista.

11. Kirjoita ominaisuuden nimi ja kuvaus ja valitse sitten **Luo ominaisuus**.

    Kun ominaisuus on luotu, siitä luodaan automaattisesti luonnosversio.

12. Valitse ominaisuuden luonnosversio ja valitse sitten **Muokkaa**. **Verolaskelman asetukset** -sivu täytetään.
13. Valitse **Määritysten versio**. Sinun pitäisi nähdä vaiheessa 8 tuotu määritysversio.

    Microsoft tarjoaa verolaskenta-apuohjelman oletusveromäärityksen. Tämä määritys kattaa suurimman osan verolaskennan vaatimuksista. Sitä päivitetään markkinapalautteen perusteella. Jos konfiguraatiota on laajennettava vastaamaan tiettyjä vaatimuksia, katso lisätietoja oman verokonfiguraation luomisesta ja valitsemisesta kohdassa [Veropalvelun laajennuksen kehittäminen](https://go.microsoft.com/fwlink/?linkid=2138483).

    Kun olet valinnut **määritysversion**, useita välilehtiä tulee näkyviin:

    - **Verokoodit** – Tämä välilehti on pakollinen verolaskentapalvelussa. Sitä käytetään verokoodien päätietojen ylläpitämiseen. Kaikki tässä välilehdessä luodut verokoodit synkronoidaan automaattisesti Financeen, kun otat käyttöön vero-ominaisuuden asetusten nykyisen version yrityksessä.
    - **Verokoodien kohdistettavuus** – Tämä välilehti on pakollinen verolaskenta-apuohjelmassa. Sen avulla määritetään matriisi, joka määrittää verokoodin, veroryhmän ja nimikkeen veroryhmän. Määritettyä verokoodia käytetään veron summan laskemiseen. **Verokoodi**-, **Veroryhmä**- ja **Nimikkeen veroryhmä** -kenttien arvot palautetaan Financeen.
    - **Asiakkaan verorekisteröintinumeron kohdistettavuus** – Tämä välilehti on valinnainen verolaskenta-apuohjelmassa. Jos yhdellä asiakkaalla on useita verorekisteröintinumeroita, verolaskelma-lisäosa voi määrittää automaattisesti oikean verorekisteröintinumeron. Tämän välilehden matriisissa määritetään säännöt, joita lisäosa käyttää tässä päättelyssä. Muutoin Finance ja Supply Chain Management jatkavat veron oletusrekisteröintinumeron käyttöä myyntitapahtumien verotettavissa asiakirjoissa.
    - **Toimittajan verorekisteröintinumeron kohdistettavuus** – Tämä välilehti on valinnainen verolaskenta-apuohjelmassa. Jos yhdellä toimittajalla on useita verorekisteröintinumeroita, verolaskelma-lisäosa voi määrittää automaattisesti oikean verorekisteröintinumeron. Tämän välilehden matriisissa määritetään säännöt, joita lisäosa käyttää tässä päättelyssä. Muutoin Finance ja Supply Chain Management jatkavat veron oletusrekisteröintinumeron käyttöä ostotapahtumien verotettavissa asiakirjoissa.
    - **Luettelokoodien kohdistettavuus** – Tämä välilehti on valinnainen verolaskenta-apuohjelmassa. Se voi auttaa määrittämään automaattisesti **Luettelokoodi**-kentän arvon joustavampien ja konfiguroitavampien sääntöjen avulla. Tämän välilehden matriisissa voit määrittää säännöt, joita lisäosa käyttää tässä päättelyssä. Muutoin Finance ja Supply Chain Management jatkavat oletuskoodin käyttöä verotettavissa asiakirjoissa.

14. Valitse **Verokoodit**-välilehdessä **Lisää** ja kirjoita verokoodi sekä kuvaus.
15. Valitse **Verokomponentti**. Verokomponentti on ryhmä veron laskentatapoja, jotka on määritetty valitun verokonfiguraation aiemmassa versiossa. Seuraavat verkokomponentit ovat käytettävissä:

    - Nettosumman mukaan
    - Bruttosumman mukaan
    - Määrän mukaan
    - Katteen mukaan
    - Veron vero

16. Valitse **Tallenna**. Käytettävissä on lisää kenttiä valitsemasi verokomponentin perusteella.
17. Määritä verokoodin luonne seuraavien vaihtoehtojen avulla:

    - On veroton
    - On käyttövero
    - On käänteinen veloitus
    - Jätä pois perussumman laskennassa

    Määritä käyttöveroskenaariossa yksi verokoodi, jonka veroprosentti on positiivinen, ja merkitse siihen **On käyttövero**.

    Määritä käänteisen veloituksen skenaariossa kaksi verokoodia, joista toisen veroprosentti on positiivinen ja toinen, jolla on negatiivinen veroprosentti mutta sama prosentin arvo. Merkitse negatiiviseen verokoodiin **On käänteinen veloitus**. Lisätietoja Financen käänteisen veloituksen ratkaisusta on kohdassa [ALV/GST-mallin käänteisen veloituksen mekanismi](emea-reverse-charge.md).
    
    Valitse verotyypeissä, jotka tulee jättää pois veron perussumman laskennasta hinnan sisältävissä tapahtumissa (kuten tulliverossa joissakin maissa) **Jätä pois perussumman laskennassa** -valintaruutu.

    Ylläpidä tämän verokoodin veroprosentteja ja verosumman rajoja.

18. Toista vaiheet 14-17 lisätäksesi kaikki muut pakolliset verokoodit.
19. Valitse **Verokoodien kohdistettavuus** -välilehdessä sarakkeet, joita tarvitaan oikean verokoodin määrittämiseen, ja valitse sitten **Lisää**.
20. Määritä tai valitse arvot kullekin sarakkeelle. **Verokoodi**-, **Veroryhmä**- ja **Nimikkeen veroryhmä** -kentät ovat tämän matriisin tulosteita.
21. Toista vaiheet 19-20 määrittääksesi asiakkaan verorekisteröintinumeroiden, toimittajien verorekisteröintinumeroiden ja luettelokoodien kohdistettavuudet.
22. Valitse **Tallenna** ja sulje sitten sivu.
23. Valitse **Muutoksen tila** \> **Viimeistele**. Kun tilaksi muutetaan **Valmis**, versiota ei voi enää muokata.
24. Valitse **Muuta tilaa** \> **Julkaise**. Tämä verotoiminnon asetusten versio työnnetään yleiseen tietovarastoon ja se näkyy kullekin Financen yritykselle.

## <a name="dynamics-365-setup"></a>Dynamics 365:n asetukset

Kun asetukset on tehty RCS:ssä edellisen osan ohjeiden mukaisesti, käytössä on vero-ominaisuuden julkaistu versio. Näiden vaiheiden avulla voit määrittää verolaskelma-apuohjelman Financessa.

Tämän osan määritykset tehdään yrityskohtaisesti. Se on määritettävä kullekin yritykselle, jolle verolaskelma-lisäosa otetaan käyttöön Financessa.

1. Siirry Financessa kohtaan **Vero** \> **Asetukset** \> **Veromääritys** \> **Verolaskelma-apuohjelman määritys (esiversio)**.
2. Määritä **Yleiset**-välilehdessä seuraavat kentät:

    - **Ota käyttöön verolaskelma-apuohjelma** – Valitsemalla tämän valintaruudun voit ottaa käyttöön verolaskelma-apuohjelman yritykselle. Jos verolaskelma-apuohjelmaa ei ole otettu käyttöön nykyiselle yritykselle, yritys käyttää edelleen aiemmin luotua veromoduulia veron määrittämiseen ja laskemiseen.
    - **Ominaisuuden määritys** – Valitse yritykselle julkaistun verotoiminnon asetukset ja versio. Lisätietoja julkaistun verotoiminnon määrittämisestä ja suorittamisesta on tämän ohjeaiheen edellisessä osassa.
    - **Liiketoimintaprosessi** – Valitse liiketoimintaprosessit, jotka otetaan käyttöön verolaskelma-apuohjelmalle.
    - **Ota verokoodin oikaisu käyttöön** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat ottaa käyttöön verokoodioikaisut arvonlisäverosivulla.

3. Määritä **Laskelma**-välilehdessä yrityksen odotettu pyöristyssääntö.
4. Määritä **Virheen käsittely** -välilehdessä yrityksen odotettu virheenkäsittelymenetelmä. Jokaiselle verolaskelma-apuohjelman tuloskoodille on käytettävissä kolme vaihtoehtoa:

    - Nro
    - Varoitus
    - Virhe

5. Tallenna verolaskelma-apuohjelman asetukset.
6. Toista vaiheet 1-5 jokaiselle lisäyritykselle.

## <a name="transaction-processing"></a>Tapahtumien käsittely

Kun olet suorittanut kaikki määritysmenettelyt, voit käyttää veron laskennan lisäosaa verojen määrittämiseen ja laskemiseen Financessa. Tapahtumien käsittelyvaiheet säilyvät samana. Financen versio 10.0.18 tukee seuraavia tapahtumia:

- Myyntiprosessi

    - Myyntitarjous
    - Myyntitilaus
    - Vahvistus
    - Materiaaliluettelo
    - Pakkausluettelo
    - Myyntilasku
    - Hyvityslasku
    - Palautustilaus
    - Otsikkomaksu
    - Riviveloitus

- Ostoprosessi

    - Ostotilaus
    - Vahvistus
    - Saapumisluettelo
    - Tuotteen vastaanotto
    - Ostolasku
    - Otsikkomaksu
    - Riviveloitus
    - Hyvityslasku
    - Palautustilaus
    - Ostoehdotus
    - Ostoehdotuksen rivin veloitus
    - Tarjouspyyntö
    - Tarjouspyynnön otsikon kulu
    - Tarjouspyynnön rivin kulu

- Varastoprosessi

    - Siirtotilaus – lähetä
    - Siirtotilaus – vastaanota
