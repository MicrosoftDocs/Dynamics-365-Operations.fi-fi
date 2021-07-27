---
title: Verolaskennan aloittaminen
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää verolaskennan.
author: wangchen
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 454608c2c3a86b71cf181129c762c837c5165902
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336653"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Verolaskennan (esiversio) käytön aloittaminen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja verolaskennan käytön aloittamisesta. Ensin se opastaa sinua Microsoft Dynamics Lifecycle Servicesin (LCS), Regulatory Configuration Servicen (RCS) ja Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin määritysvaiheissa. Tämän jälkeen se tarkastelee yleistä prosessia, jossa veronlaskennan mahdollisuuksia käytetään Financen ja Supply Chain Managementin tapahtumissa.

Asetukset koostuvat neljästä päävaihesta:

1. Asenna verolaskenta LCS:ssä.
2. Määritä RCS:ssä veronlaskentaominaisuus. Nämä määritykset eivät ole yrityskohtaisia. Se voidaan jakaa Financen ja Supply Chain Managementin oikeushenkilöiden kanssa.
3. Määritä Financessa ja Supply Chain Managementissa verolaskennan parametrit oikeushenkilöittäin.
4. Luo Financessa ja Supply Chain Managementissa tapahtumia, kuten myyntitilauksia, ja määritä ja laske verot verolaskennan avulla.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän ohjeaiheen vaiheita, seuraavien edellytysten on toteuduttava:

- Voit käyttää LCS-tiliäsi ja olet ottanut käyttöön LCS-projektin, jossa on taso 2 (tai korkeampi) ympäristö, jossa on Dynamics 365:n versio 10.0.18 ja [KB4616360](https://fix.lcs.dynamics.com/Issue/Details?kb=4616360&bugId=568738&dbType=3&qc=1f1c04ff39adad74ef871f539e8d73e14c1893ef7cc4b6e3f7d5c5864ec2781a) tai uudempi.
- Sinull on pääsy RCS-tiliisi.
- Olet ottanut yhteyttä Microsoftiin ottaaksesi väliversiot käyttöön ottamassasi Finance- tai Supply Chain Management -ympäristössä.

## <a name="set-up-tax-calculation-in-lcs"></a>Määritä verolaskenta LCS:ssä

1. Kirjaudu [LCS-palveluun](https://lcs.dynamics.com)
2. Viimeistele Microsoft Power Platform -integroinnin asetukset. Lisätietoja on kohdassa [Apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Valitse jokin käyttöön otettu muu kuin tuotantoympäristö ja valitse sitten **Asenna uusi apuohjelma**.
4. Valitse **Verolaskelma (esiversio)**.
5. Lue ja hyväksy käyttöehdot ja valitse sitten **Asenna**.

## <a name="set-up-tax-calculation-in-rcs"></a>Määritä verolaskenta RCS:ssä

Tämän osan vaiheet eivät liity tiettyyn oikeushenkilöön. Sinun on suoritettava tämä toiminto vain kerran, ja voit suorittaa sen missä tahansa RCS:n oikeushenkilössä.

1. Kirjaudu sisään [RCS:ään](https://marketing.configure.global.dynamics.com/).
2. Valitse **Sähköinen raportointi** -työtila, lisää uusi määrityspalvelu. Käytä yrityksesi nimeä palveluntarjoajan nimenä. Lisätietoja on kohdassa [Määrityspalvelujen luonti ja merkitseminen aktiiviseksi](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Valitse juuri luomasi määrityspalvelu ja valitse sitten **Aseta aktiiviseksi**.
4. Valitse **Microsoft**-määrityspalvelu ja valitse sitten **Säilöt**.
5. Kirjoita **Tyyppi**-kenttään **Yleinen**.
6. Valitse **Avaa**.
7. Siirry kohtaan **Verotietomalli**, laajenna tiedostopuu ja valitse sitten **Veromääritys**.
8. Valitse uusin versio ja valitse sitten **Tuo**.
9. Palaa **Globalisaatio-ominaisuudet (esiversio)** -työtilaan, valitse **Ominaisuudet**, valitse **Verolaskelma**-ruutu ja valitse sitten **Lisää**.
10. Valitse jokin seuraavista ominaisuustyypeistä:

    - **Uusi ominaisuus** – Luo ominaisuusasetus, jonka sisältö on tyhjä.
    - **Aiemmin luodun ominaisuuden perusteella** – Luo ominaisuus aiemmin luodusta ominaisuudesta ja kopioi sisältö aiemmin luoduista ominaisuusasetuksista.

11. Kirjoita ominaisuuden nimi ja kuvaus ja valitse sitten **Luo ominaisuus**.

    Kun ominaisuus on luotu, siitä luodaan automaattisesti luonnosversio.

12. Valitse ominaisuuden luonnosversio ja valitse sitten **Muokkaa**. **Verolaskelman asetukset** -sivu täytetään.
13. Valitse **Määritysten versio**. Sinun pitäisi nähdä vaiheessa 8 tuotu määritysversio.

    Microsoft tarjoaa verolaskenta-apuohjelman oletusveromäärityksen. Tämä määritys kattaa suurimman osan verolaskennan vaatimuksista. Sitä päivitetään markkinapalautteen perusteella. Jos konfiguraatiota on laajennettava vastaamaan tiettyjä vaatimuksia, katso lisätietoja oman verokonfiguraation luomisesta ja valitsemisesta kohdassa [Veropalvelun laajennuksen kehittäminen](./tax-service-add-data-fields-tax-integration-by-extension.md).

    Kun olet valinnut **määritysversion**, useita välilehtiä tulee näkyviin:

    - **Verokoodit** – Tämä välilehti on pakollinen. Sitä käytetään verokoodien päätietojen ylläpitämiseen. Kaikki tässä välilehdessä luodut verokoodit synkronoidaan automaattisesti Financeen, kun otat käyttöön vero-ominaisuuden asetusten nykyisen version yrityksessä.
    - **Verokoodien sovellettavuus** – Tämä välilehti on pakollinen. Sen avulla määritetään matriisi, joka määrittää verokoodin, veroryhmän ja nimikkeen veroryhmän. Määritettyä verokoodia käytetään veron summan laskemiseen. **Verokoodi**-, **Veroryhmä**- ja **Nimikkeen veroryhmä** -kenttien arvot palautetaan Financeen.
    - **Asiakkaan verorekisteröintinumeron kohdistettavuus** – Tämä välilehti on valinnainen. Jos yhdellä asiakkaalla on useita verorekisteröintinumeroita, verolaskenta voi määrittää automaattisesti oikean verorekisteröintinumeron. Tämän välilehden matriisissa määritetään säännöt, joita käytetään tässä päättelyssä. Muutoin Finance ja Supply Chain Management jatkavat veron oletusrekisteröintinumeron käyttöä myyntitapahtumien verotettavissa asiakirjoissa.
    - **Alihankkijan verorekisteröintinumeron kohdistettavuus** – Tämä välilehti on valinnainen. Jos yhdellä alihankkijalla on useita verorekisteröintinumeroita, verolaskenta voi määrittää automaattisesti oikean verorekisteröintinumeron. Tämän välilehden matriisissa määritetään säännöt, joita käytetään tässä päättelyssä. Muutoin Finance ja Supply Chain Management jatkavat veron oletusrekisteröintinumeron käyttöä ostotapahtumien verotettavissa asiakirjoissa.
    - **Luettelokoodin käytettävyys** – Tämä välilehti on valinnainen. Se voi auttaa määrittämään automaattisesti **Luettelokoodi**-kentän arvon joustavampien ja konfiguroitavampien sääntöjen avulla. Tämän välilehden matriisissa voidaan määrittää säännöt, joita käytetään tässä päättelyssä. Muutoin Finance ja Supply Chain Management jatkavat oletuskoodin käyttöä verotettavissa asiakirjoissa.

14. Valitse **Verokoodit**-välilehdessä **Lisää** ja kirjoita verokoodi sekä kuvaus.
15. Valitse **Verokomponentti**. Verokomponentti on ryhmä tapoja, jotka on määritetty valitun verokonfiguraation aiemmassa versiossa. Seuraavat verkokomponentit ovat käytettävissä:

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

Kun asetukset on tehty RCS:ssä edellisen osan ohjeiden mukaisesti, käytössä on vero-ominaisuuden julkaistu versio. Näiden vaiheiden avulla voit määrittää verolaskennan Financessa.

Tämän osan määritykset tehdään yrityskohtaisesti. Se on määritettävä kullekin yritykselle, jolle verolaskenta otetaan käyttöön Financessa.

1. Siirry Financessa kohtaan **Vero** \> **Asetukset** \> **Veromääritys** \> **Verolaskennan määritys (esiversio)**.
2. Määritä **Yleiset**-välilehdessä seuraavat kentät:

    - **Ota käyttöön verolaskenta** – Valitsemalla tämän valintaruudun voit ottaa käyttöön verolaskennan yritykselle. Jos sitä ei ole otettu käyttöön nykyiselle yritykselle, yritys käyttää edelleen aiemmin luotua veromoduulia veron määrittämiseen ja laskemiseen.
    - **Ominaisuuden määritys** – Valitse yritykselle julkaistun verotoiminnon asetukset ja versio. Lisätietoja julkaistun verotoiminnon määrittämisestä ja suorittamisesta on tämän ohjeaiheen edellisessä osassa.
    - **Liiketoimintaprosessi** – Valitse käyttöön otettavat liiketoimintaprosessit.
    - **Ota verokoodin oikaisu käyttöön** – Määritä tämän asetuksen arvoksi **Kyllä**, jos haluat ottaa käyttöön verokoodioikaisut arvonlisäverosivulla.

3. Määritä **Laskelma**-välilehdessä yrityksen odotettu pyöristyssääntö.
4. Määritä **Virheen käsittely** -välilehdessä yrityksen odotettu virheenkäsittelymenetelmä. Tuloskoodille on käytettävissä kolme vaihtoehtoa:

    - Nro
    - Varoitus
    - Virhe

5. Tallenna asetukset.
6. Toista vaiheet 1-5 jokaiselle lisäyritykselle.

## <a name="transaction-processing"></a>Tapahtumien käsittely

Kun olet suorittanut kaikki määritysmenettelyt, voit käyttää veron laskentaa verojen määrittämiseen ja laskemiseen Financessa. Tapahtumien käsittelyvaiheet säilyvät samana. Financen versio 10.0.18 tukee seuraavia tapahtumia:

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
