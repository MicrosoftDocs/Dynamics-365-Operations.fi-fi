---
title: Verolaskennan aloittaminen
description: Tässä ohjeaiheessa kuvataan, kuinka voit määrittää verolaskennan.
author: wangchen
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1ddbb22d4f7c6108ca93b415276c53794b5450dd
ms.sourcegitcommit: 03f53980a4bc67b73ac2be76a3b3e7331d0db705
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/18/2021
ms.locfileid: "7394506"
---
# <a name="get-started-with-tax-calculation"></a>Verolaskennan aloittaminen

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Tässä ohjeaiheessa on tietoja verolaskennan käytön aloittamisesta. Se auttaa määrittämään Microsoft Dynamics Lifecycle Servicesin (LCS), Regulatory Configuration Servicen (RCS) ja Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin. Tämän jälkeen se tarkastelee yleistä prosessia, jossa veronlaskennan mahdollisuuksia käytetään Financen ja Supply Chain Managementin tapahtumissa.

Asetukset koostuvat neljästä päävaihesta:

1. Asenna LCS:ssä verolaskennan apuohjelma.
2. Määritä RCS:ssä veronlaskentaominaisuus. Nämä määritykset eivät ole yrityskohtaisia. Se voidaan jakaa Financen ja Supply Chain Managementin oikeushenkilöiden kanssa.
3. Määritä Financessa ja Supply Chain Managementissa verolaskennan parametrit oikeushenkilöittäin.
4. Luo Financessa ja Supply Chain Managementissa tapahtumia, kuten myyntitilauksia, ja määritä ja laske verot verolaskennan avulla.

## <a name="prerequisites"></a>Edellytykset

Ennen tämän aiheen ohjeiden mukaan toimimista seuraavien edellytysten on toteuduttava kussakin ympäristötyypissä.

### <a name="for-a-production-environment"></a>Tuotantoympäristö

Seuraavien edellytysten on toteuduttava tuotantoympäristössä:

- LCS-tilin käyttöoikeus ja sellainen käyttöönotettu LCS-projekti, jonka vähintään tason 2 ympäristössä on käytössä Dynamics 365:n versio 10.0.21 tai uudempi.
- Organisaatiolle on luotava RCS-ympäristö ja käytössä on oltava tilin käyttöoikeus. Lisätietoja RCS-ympäristön luomisesta on kohdassa [Regulatory Configuration Servicen yleiskatsaus](rcs-overview.md).
- Seuraavat toiminnot on otettava käyttöön liiketoimintatarpeiden mukaan käyttöönotetun Finance- tai Supply Chain Management -ympäristön **Ominaisuuksien hallinta** -työtilassa:

    - Verolaskenta
    - Tue useita ALV-rekisteröintinumeroita
    - Vero siirtotilauksessa
    - EU-myyntiluettelon siirto vain verotapahtumien perusteella
    - Intrastat-raportointi usean verotunnuksen mukaan
    - EU-myyntiluettelon raportointi usean verotunnuksen mukaan
    - Arvonlisäverotilitys usean verotunnuksen mukaan

- Seuraavat toiminnot on otettava käyttöön käyttöönotetun RCS-ympäristön **Ominaisuuksien hallinta** -työtilassa.

    - Globalisaatio-ominaisuudet

### <a name="for-a-test-environment-public-preview"></a>Testiympäristö (julkinen esiversio)

Seuraavien edellytysten on toteuduttava testiympäristössä:

- LCS-tilin käyttöoikeus ja sellainen käyttöönotettu LCS-projekti, jonka vähintään tason 2 ympäristössä on käytössä Dynamics 365:n versio 10.0.18 ja KB4616360 tai uusin versio.
- Organisaatiolle on luotava RCS-ympäristö ja käytössä on oltava tilin käyttöoikeus. Lisätietoja RCS-ympäristön luomisesta on kohdassa [Regulatory Configuration Servicen yleiskatsaus](rcs-overview.md).
- Väliversioiden ottaminen käyttöön käyttöönotetussa Finance- tai Supply Chain Management -ympäristössä edellyttää yhteydenottoa Microsoftiin lähettämällä sähköpostia osoitteeseen <taxcalc@microsoft.com>.
- Seuraavat toiminnot on otettava käyttöön liiketoimintatarpeiden mukaan käyttöönotetun Finance- tai Supply Chain Management -ympäristön **Ominaisuuksien hallinta** -työtilassa:

    - Verolaskenta
    - Tue useita ALV-rekisteröintinumeroita
    - Vero siirtotilauksessa
    - EU-myyntiluettelon siirto vain verotapahtumien perusteella
    - Intrastat-raportointi usean verotunnuksen mukaan
    - EU-myyntiluettelon raportointi usean verotunnuksen mukaan
    - Arvonlisäverotilitys usean verotunnuksen mukaan

- Seuraavat toiminnot on otettava käyttöön käyttöönotetun RCS-ympäristön **Ominaisuuksien hallinta** -työtilassa.

    - Globalisaatio-ominaisuudet

## <a name="set-up-tax-calculation-in-lcs"></a>Määritä verolaskenta LCS:ssä

1. Kirjaudu [LCS-palveluun](https://lcs.dynamics.com)
2. Viimeistele Microsoft Power Platform -integroinnin asetukset. Lisätietoja on kohdassa [Apuohjelmien yleiskatsaus](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md).
3. Valitse jokin käyttöönotettu ympäristö ja valitse sitten **Asenna uusi apuohjelma**.
4. Valitse **Verolaskenta**.
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
8. Valitse oikea veromääritysversio Finance-version perusteella ja valitse sitten **Tuo**.

    | Julkaisuversio | Verokonfiguraatio                       | Mallin määritys                   |
    | --------------- | --------------------------------------- | ------------------------------- |
    | 10.0.18         | Veromääritys – Eurooppa 30.12.82     |                                 |
    | 10.0.19         | Verolaskentamääritys 36.38.193 |                                 |
    | 10.0.20         | Verolaskentamääritys 40.43.208 |                                 |
    | 10.0.21         | Verolaskentamääritys 40.46.212 | Dataverse-mallin yhdistämismääritys 40.46.9 |

9. Valitse **Globalisaatio-ominaisuudet** -työtilaan, valitse **Ominaisuudet**, valitse **Verolaskenta**-ruutu ja valitse sitten **Lisää**.
10. Valitse jokin seuraavista ominaisuustyypeistä:

    - **Uusi ominaisuus** – Luo ominaisuusasetus, jonka sisältö on tyhjä.
    - **Aiemmin luodun ominaisuuden perusteella** – Luo ominaisuus aiemmin luodusta ominaisuudesta ja kopioi sisältö aiemmin luoduista ominaisuusasetuksista.

11. Kirjoita ominaisuuden nimi ja kuvaus ja valitse sitten **Luo ominaisuus**.

    Kun ominaisuus on luotu, siitä luodaan automaattisesti luonnosversio. Valitsemalla **Hae tämä versio** luonnosversion veroperustetta voidaan muuttaa missä tahansa valmiissa versiossa.

12. Valitse ominaisuuden luonnosversio ja valitse sitten **Muokkaa**. **Verolaskelman asetukset** -sivu täytetään.
13. Valitse **Määritysten versio**. Sinun pitäisi nähdä vaiheessa 8 tuotu määritysversio.

    Microsoftilla toimittaa verolaskennan oletusveromääritys. Tämä määritys kattaa suurimman osan verolaskennan vaatimuksista. Sitä päivitetään markkinapalautteen perusteella. Jos konfiguraatiota on laajennettava vastaamaan tiettyjä vaatimuksia, katso lisätietoja oman verokonfiguraation luomisesta ja valitsemisesta kohdassa [Veropalvelun laajennuksen kehittäminen](./tax-service-add-data-fields-tax-integration-by-extension.md).

14. **Määritysversion** valinnan jälkeen avautuu useita lisävälilehtiä. Suorita välilehden pakollinen määritys tässä näkyvässä järjestyksessä.

    **Pakolliset asetukset**

    - **Verokoodit** – Käytetään verokoodien päätietojen ylläpitämiseen. Kaikki tässä välilehdessä luodut verokoodit synkronoidaan automaattisesti Financeen, kun nykyinen versio otetaan käyttöön.
    - **Veroryhmä** – veroryhmän päätietojen ja ryhmän verokoodien määrittäminen.
    - **Nimikkeen veroryhmä** – nimikkeen veroryhmän päätietojen ja ryhmän verokoodien määrittäminen.

    **Valinnaiset asetukset**

    - **Veroryhmän käytettävyys** – Veroryhmän määrittävän matriisin määrittäminen. Jos mikään matriisin käytettävyyssääntö ei vastaa Dynamics 365:n verotettavaa asiakirjaa, verolaskenta käyttää oletusarvo verotettavalla asiakirjarivillä.
    - **Nimikkeen veroryhmän käytettävyys** – Nimikkeen veroryhmän määrittävän matriisin määrittäminen. Jos mikään matriisin käytettävyyssääntö ei vastaa Dynamics 365:n verotettavaa asiakirjaa, verolaskenta käyttää oletusarvo verotettavalla asiakirjarivillä.
    - **Asiakkaan verorekisteröintinumeron käytettävyys** – Jos yhdellä asiakkaalla on useita verorekisteröintinumeroita, verolaskenta voi määrittää automaattisesti oikean verorekisteröintinumeron. Tämän välilehden matriisissa määritetään säännöt, joita on käytettävä määrityksessä. Muutoin Finance ja Supply Chain Management jatkavat veron oletusrekisteröintinumeron käyttöä myyntitapahtumien verotettavissa asiakirjoissa.
    - **Toimittajan verorekisteröintinumeron käytettävyys** – Jos yhdellä toimittajalla on useita verorekisteröintinumeroita, verolaskenta voi määrittää automaattisesti oikean verorekisteröintinumeron. Tämän välilehden matriisissa määritetään säännöt, joita on käytettävä määrityksessä. Muutoin Finance ja Supply Chain Management jatkavat veron oletusrekisteröintinumeron käyttöä ostotapahtumien verotettavissa asiakirjoissa.
    - **Luettelokoodin käytettävyys** – Määrittää automaattisesti **Luettelokoodi**-kentän arvon entistä joustavampien ja määrittävämpien sääntöjen avulla. Tämän välilehden matriisissa määritetään säännöt, joita on käytettävä määrityksessä. Muutoin Finance ja Supply Chain Management jatkavat oletuskoodin käyttöä verotettavissa asiakirjoissa.

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

    Määritä käyttöveroskenaariossa yksi verokoodi, jonka veroprosentti on positiivinen, ja merkitse se **On käyttövero** -vaihtoehtona.

    Määritä käänteisen veloituksen skenaariossa kaksi verokoodia, joista toisen veroprosentti on positiivinen ja toinen, jolla on negatiivinen veroprosentti mutta sama prosentin arvo. Merkitse negatiiviseen verokoodiin **On käänteinen veloitus**. Lisätietoja Financen käänteisen veloituksen ratkaisusta on kohdassa [ALV/GST-mallin käänteisen veloituksen mekanismi](emea-reverse-charge.md).

    Valitse verotyypeissä, jotka on jätettävä pois veron perussumman laskennasta hinnan sisältävissä tapahtumissa (kuten joidenkin maiden tai alueiden tullimaksussa) **Jätä pois perussumman laskennassa** -valintaruutu. Lisätietoja tästä parametrista on kohdassa [Veron laskeminen hinnan päälle, kun hinnat sisältävät verot on otettu käyttöön](global-exclude-from-tax-base-amount-calculation.md).

    Ylläpidä tämän verokoodin veroprosentteja ja verosumman rajoja.

18. Toista vaiheet 14-17 lisätäksesi kaikki muut pakolliset verokoodit.
19. Valitse **Veroryhmä**-välilehdessä **Veroryhmä**-sarake, lisää se matriisiin syöttöehdon ja lisää sitten rivit ylläpitämään veroryhmän päätietoja.

    Esimerkki:

    | Veroryhmä    | Verokoodit           |
    | ------------ | ------------------- |
    | DEU_Domestic | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Domestic | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

20. Valitse **Nimikkeen veroryhmä**-välilehdessä **Nimikkeen veroryhmä**-sarake, lisää se matriisiin syöttöehdon ja lisää sitten rivit ylläpitämään nimikkeen veroryhmän päätietoja.

    Esimerkki:

    | Nimikkeen veroryhmä | Verokoodit                                    |
    | -------------- | -------------------------------------------- |
    | Täysi           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Vähennetty        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

21. Valitse **Veroryhmän käytettävyys** -välilehdessä sarakkeet, joita tarvitaan oikean veroryhmän määrittämiseen, ja valitse sitten **Lisää**. Määritä tai valitse arvot kullekin sarakkeelle. **Veroryhmä**-kenttä on tämän matriisin tuotos. Jos tätä välilehteä ei määritetä, tapahtumarivin arvonlisäveroryhmää käytetään.

    Esimerkki:

    | Liiketoimintaprosessi | Lähettäjän osoite | Toimitusosoite | Veroryhmä    |
    | ---------------- | --------- | ------- | ------------ |
    | Myynti            | DEU       | DEU     | DEU_Domestic |
    | Myynti            | DEU       | FRA     | DEU_EU       |
    | Myynti            | BEL       | BEL     | BEL_Domestic |
    | Myynti            | BEL       | FRA     | BEL_EU       |

22. Valitse **Nimikkeen veroryhmän käytettävyys** -välilehdessä sarakkeet, joita tarvitaan oikean verokoodin määrittämiseen, ja valitse sitten **Lisää**. Määritä tai valitse arvot kullekin sarakkeelle. **Nimikkeen veroryhmä** -kenttä on tämän matriisin tuotos. Jos tätä välilehteä ei määritetä, tapahtumarivin nimikkeen arvonlisäveroryhmää käytetään.

    Esimerkki:

    | Nimikekoodi | Nimikkeen veroryhmä |
    | --------- | -------------- |
    | D0001     | Täysi           |
    | D0003     | Vähennetty        |

    Lisätietoja verokoodien määrittämisestä verolaskennassa on kohdassa [Arvolisäveroryhmän ja nimikkeen arvonlisäveroryhmän määrityslogiikka](global-sales-tax-group-determination.md).

23. Määritä asiakkaan verorekisteröintinumeroiden, toimittajien verorekisteröintinumeroiden ja luettelokoodien käytettävyydet liiketoimintatarpeiden perusteella.
24. Valitse **Tallenna** ja sulje sitten sivu.
25. Valitse **Muutoksen tila** \> **Viimeistele**. Kun tilaksi muutetaan **Valmis**, versiota ei voi enää muokata.
26. Valitse **Muuta tilaa** \> **Julkaise**. Tämä verotoiminnon asetusten versio työnnetään yleiseen tietovarastoon ja se näkyy kullekin Financen yritykselle.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Verolaskennan määrittäminen Dynamics 365:ssä

Kun RCS-määritykset on tehty, käytössä on verotoiminnon julkaistu versio. Näiden vaiheiden avulla voit määrittää verolaskennan Financessa.

Tämän osan määritykset tehdään yrityskohtaisesti. Se on määritettävä kullekin yritykselle, jolle verolaskenta otetaan käyttöön Financessa.

1. Valitse Financessa **Vero** \> **Asetukset** \> **Veromääritys** \> **Verolaskennan parametrit**.
2. Määritä **Yleiset**-välilehdessä seuraavat kentät:

    - **Ota verolaskentapalvelu käyttöön** – Verolaskentaa voidaan ottaa käyttöön yrityksessä valitsemalla tämä valintaruutu. Jos sitä ei ole otettu käyttöön nykyiselle yritykselle, yritys käyttää edelleen aiemmin luotua veromoduulia veron määrittämiseen ja laskemiseen.
    - **Ominaisuuden määritys** – Valitse yritykselle julkaistun verotoiminnon asetukset ja versio. Lisätietoja julkaistun verotoiminnon määrittämisestä ja suorittamisesta on tämän ohjeaiheen edellisessä osassa.
    - **Liiketoimintaprosessi** – Valitse käyttöön otettavat liiketoimintaprosessit.

3. Määritä **Laskelma**-välilehdessä yrityksen odotettu pyöristyssääntö. Lisätietoja pyöristyslogiikasta on kohdassa [Verolaskennan pyöristyssäännöt](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Määritä **Virheen käsittely** -välilehdessä yrityksen odotettu virheenkäsittelymenetelmä. Käytössä on kolme vaihtoehtoa:

    - Nro
    - Varoitus
    - Virhe

    Kunkin tuloskoodin virheiden käsittelymenetelmä määritetään **Tiedot**-osassa. Jos joitakin tuloskoodeja ei synkronoida verolaskentapalvelusta, oletusmenetelmä voidaan vaihtoehtoisesti määrittää **Yleiset**-osassa.

5. **Useita ALV-rekisteröintejä** -välilehdessä ALV-ilmoitus, EU:n arvonlisäveron yhteenvetoilmoitus ja Intrastat-ilmoitus voidaan ottaa erikseen käyttöön, jos kyse on useita ALV-rekisteröintejä käyttävästä skenaariosta. Lisätietoja useiden ALV-rekisteröintien veroilmoituksesta on kohdassa [Useiden ALV-rekisteröintien raportointi](emea-reporting-for-multiple-vat-registrations.md).
6. Tallenna määritykset ja toista edelliset vaiheet kunkin yrityksen kohdalla. Julkaistua uuttaa versiota voidaan käyttää tekemällä määritys **Verolaskennan parametrit** -sivun **Yleiset**-välilehden **Ominaisuuden asetus** -kentässä (katso vaihe 2).

## <a name="transaction-processing"></a>Tapahtumien käsittely

Kun kaikki määritykset ovat valmiita, verolaskentaa voi käyttää verojen määrittämiseen ja laskemiseen Financessa. Tapahtumien käsittelyvaiheet säilyvät samana. Financen versio 10.0.21 tukee seuraavia tapahtumia:

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
