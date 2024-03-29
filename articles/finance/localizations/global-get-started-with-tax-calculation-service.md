---
title: Verolaskennan aloittaminen
description: Tässä artikkelissa kuvataan, kuinka voit määrittää verolaskennan.
author: EricWangChen
ms.date: 10/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.custom: intro-internal
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 42898823ffc366351c6f58f1fe9b924678ab4b49
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690380"
---
# <a name="get-started-with-tax-calculation"></a>Verolaskennan aloittaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa on tietoja verolaskennan käytön aloittamisesta. Tämän artikkelin osat opastavat sinua Microsoft Dynamics Lifecycle Servicesin (LCS), Regulatory Configuration Servicen (RCS) ja Dynamics 365 Financen ja Dynamics 365 Supply Chain Managementin korkean tason suunnittelu- ja määritysvaiheissa. 

Asetukset koostuvat kolmesta päävaiheesta.

1. Asenna LCS:ssä verolaskennan apuohjelma.
2. Määritä RCS:ssä veronlaskentaominaisuus. Nämä määritykset eivät ole yrityskohtaisia. Se voidaan jakaa Financen ja Supply Chain Managementin oikeushenkilöiden kanssa.
3. Määritä Financessa ja Supply Chain Managementissa verolaskennan parametrit oikeushenkilöittäin.

## <a name="high-level-design"></a>Korkean tason rakenne

### <a name="runtime-design"></a><a name="runtime"></a> Suorituksenaikainen rakenne

Seuraavassa kuvassa esitellään verolaskennan korkean tason suorituksenaikainen rakenne. Koska verolaskenta voidaan integroida useisiin Dynamics 365 -sovelluksiin, havainnollistuksessa käytetään esimerkkinä Finance-integrointia.

1. Financessa luodaan tapahtuma, kuten myyntitilaus tai ostotilaus.
2. Finance käyttää automaattisesti arvonlisäveroryhmän ja nimikkeen arvonlisäveroryhmän oletusarvoja.
3. Kun tapahtuman **Arvonlisävero**-painike on valittuna, verolaskenta käynnistyy. Finance lähettää sitten tiedot verolaskentapalveluun.
4. Arvonlisäveron laskentapalvelu etsii tiedoille vastaavuuden verotoiminnon ennalta määritetyillä säännöillä, jotta löydetään tarkempi arvonlisäveroryhmä ja nimikkeen arvonlisäveroryhmä samanaikaisesti.

    - Jos tiedot voidaan yhdistää **Veroryhmän käytettävyys** -matriisiin, se korvaa arvonlisäveroryhmän arvon sovellettavuussäännön veroryhmän arvolla. Muuten se jatkaa Financen arvonlisäveroryhmän arvon käyttöä.
    - Jos tiedot voidaan yhdistää **Nimikkeen veroryhmän käytettävyys** -matriisiin, se korvaa nimikkeen arvonlisäveroryhmän arvon sovellettavuussäännön nimikkeen veroryhmän arvolla. Muuten se jatkaa Financen nimikkeen arvonlisäveroryhmän arvon käyttöä.

5. Veron laskentapalvelu määrittää lopulliset verokoodit arvonlisäveroryhmän ja nimikkeen arvonlisäveroryhmän leikkauksen avulla.
6. Veron laskentapalvelu laskee veron määrittämiensä lopullisten verokoodien perusteella.
7. Veron laskentapalvelu palauttaa veron laskennan tuloksen Financeen.

![Verolaskennan suoritusaikainen rakenne.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Korkean tason konfiguraatio

Seuraavissa vaiheissa on korkean tason yleiskuvaus verolaskentapalvelun konfigurointiprosessista.

1. Asenna LCS:ssä **Verolaskenta**-apuohjelma LCS-projektissa.
2. Luo RCS:ssä **Verolaskenta**-ominaisuus.
3. Määritä RCS:ssä **Verolaskenta**-ominaisuus:

    1. Valitse veromäärityksen versio.
    2. Luo verokoodit.
    3. Veroryhmän luominen.
    4. Luo nimikkeiden veroryhmä.
    5. Valinnainen: Luo veroryhmän käytettävyys, jos haluat ohittaa asiakkaan tai toimittajan päätietoihin kirjoitettavan oletusarvoisen arvonlisäveroryhmän.
    6. Valinnainen: Luo nimikeryhmän käytettävyys, jos haluat ohittaa nimikkeen päätietoihin kirjoitettavan oletusarvoisen nimikkeen arvonlisäveroryhmän.

4. Täydennä ja julkaise **Verolaskenta**-ominaisuus RCS:ssä.
5. Valitse Financessa julkaisu **Verolaskenta**-toiminto.

Kun olet suorittanut nämä vaiheet, seuraavat asetukset synkronoidaan automaattisesti RCS:stä Financeen.

- Arvonlisäverokoodit
- Arvonlisäveroryhmät
- Nimikkeiden arvonlisäveroryhmät

Loput tämän artikkelin osat sisältävät tarkempia tietoja määritysvaiheista.

## <a name="prerequisites"></a>Edellytykset

Ennen kuin voit suorittaa tämän artikkelin loput vaiheet, seuraavien edellytysten on toteuduttava:<!--TO HERE-->

- LCS-tilin käyttöoikeus ja sellainen käyttöönotettu LCS-projekti, jonka vähintään tason 2 ympäristössä on käytössä Dynamics 365:n versio 10.0.21 tai uudempi.
- Organisaatiolle on luotava RCS-ympäristö ja käytössä on oltava tilin käyttöoikeus. Lisätietoja RCS-ympäristön luomisesta on kohdassa [Regulatory Configuration Servicen yleiskatsaus](rcs-overview.md).
- Seuraavat toiminnot on otettava käyttöön liiketoimintatarpeiden mukaan käyttöönotetun Finance- tai Supply Chain Management -ympäristön **Ominaisuuksien hallinta** -työtilassa:

    - Verolaskentapalvelu
    - Tue useita ALV-rekisteröintinumeroita
    - Vero siirtotilauksessa

- Seuraavat toiminnot on otettava käyttöön käyttöönotetun RCS-ympäristön **Ominaisuuksien hallinta** -työtilassa.

    - Globalisaatio-ominaisuudet

- Seuraavien roolien tulee olla määritettyinä käyttäjille RCS-ympäristössäsi:

    - Sähköisen raportoinnin kehittäjä
    - Globalisaatio-ominaisuuden kehittäjä
    - Veromoduulin kehittäjä
    - Veromoduulin toiminnallinen konsultti
    - Veropalvelun kehittäjä

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
8. Valitse oikea [veromääritysversio](global-tax-calcuation-service-overview.md#versions) Finance-version perusteella ja valitse sitten **Tuo**.
9. Valitse **Globalisaatio-ominaisuudet** -työtilaan, valitse **Ominaisuudet**, valitse **Verolaskenta**-ruutu ja valitse sitten **Lisää**.

    > [!NOTE]
    > Versiossa 10.0.26 ja tätä uudemmissa versioissa on mahdollista tuoda esittelyominaisuus **DEMF**-esittely-yritykseen. Lisätietoja on kohdassa [Ominaisuuden esittelytietojen tuominen](tax-calculation-import-export-feature.md).

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

15. Valitse **Verokoodit**-välilehdessä **Lisää** ja kirjoita verokoodi sekä kuvaus.
16. Valitse **Verokomponentti**. Verokomponentti on ryhmä tapoja, jotka on määritetty valitun verokonfiguraation aiemmassa versiossa. Seuraavat verkokomponentit ovat käytettävissä:

    - Nettosumman mukaan
    - Bruttosumman mukaan
    - Määrän mukaan
    - Katteen mukaan
    - Veron vero

17. Valitse **Tallenna**. Käytettävissä on lisää kenttiä valitsemasi verokomponentin perusteella.
18. Määritä verokoodin luonne seuraavien vaihtoehtojen avulla:

    - On veroton
    - On käyttövero
    - On käänteinen veloitus
    - Jätä pois perussumman laskennassa

    Määritä käyttöveroskenaariossa yksi verokoodi, jonka veroprosentti on positiivinen, ja merkitse se **On käyttövero** -vaihtoehtona.

    Määritä käänteisen veloituksen skenaariossa kaksi verokoodia, joista toisen veroprosentti on positiivinen ja toinen, jolla on negatiivinen veroprosentti mutta sama prosentin arvo. Merkitse negatiiviseen verokoodiin **On käänteinen veloitus**. Lisätietoja Financen käänteisen veloituksen ratkaisusta on kohdassa [ALV/GST-mallin käänteisen veloituksen mekanismi](emea-reverse-charge.md).

    Valitse verotyypeissä, jotka on jätettävä pois veron perussumman laskennasta hinnan sisältävissä tapahtumissa (kuten joidenkin maiden tai alueiden tullimaksussa) **Jätä pois perussumman laskennassa** -valintaruutu. Lisätietoja tästä parametrista on kohdassa [Veron laskeminen hinnan päälle, kun hinnat sisältävät verot on otettu käyttöön](global-exclude-from-tax-base-amount-calculation.md).

    Ylläpidä tämän verokoodin veroprosentteja ja verosumman rajoja.

19. Toista vaiheet 15-18 lisätäksesi kaikki muut pakolliset verokoodit.
20. Valitse **Veroryhmä**-välilehdessä **Veroryhmä**-sarake, lisää se matriisiin syöttöehdon ja lisää sitten rivit ylläpitämään veroryhmän päätietoja.

    Esimerkki:

    | Veroryhmä    | Verokoodit           |
    | ------------ | ------------------- |
    | DEU_Dom | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Dom | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

21. Valitse **Nimikkeen veroryhmä**-välilehdessä **Nimikkeen veroryhmä**-sarake, lisää se matriisiin syöttöehdon ja lisää sitten rivit ylläpitämään nimikkeen veroryhmän päätietoja.

    Esimerkki:

    | Nimikkeen veroryhmä | Verokoodit                                    |
    | -------------- | -------------------------------------------- |
    | Täysi           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Vähennetty        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

22. Valitse **Veroryhmän käytettävyys** -välilehdessä sarakkeet, joita tarvitaan oikean veroryhmän määrittämiseen, ja valitse sitten **Lisää**. Määritä tai valitse arvot kullekin sarakkeelle. **Veroryhmä**-kenttä on tämän matriisin tuotos. Jos tätä välilehteä ei määritetä, tapahtumarivin arvonlisäveroryhmää käytetään.

    Esimerkki:

    | Liiketoimintaprosessi | Lähettäjän osoite | Toimitusosoite | Veroryhmä    |
    | ---------------- | --------- | ------- | ------------ |
    | Myynti            | DEU       | DEU     | DEU_Dom |
    | Myynti            | DEU       | FRA     | DEU_EU       |
    | Myynti            | BEL       | BEL     | BEL_Dom |
    | Myynti            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Jos verotettavan asiakirjan rivien oletusarvoinen arvonlisäveroryhmä on oikein, jätä tämä matriisi tyhjäksi. Lisätietoja on myöhemmin tämän artikkelin [Suorituksenaikainen rakenne](#runtime) -osassa.

23. Valitse **Nimikkeen veroryhmän käytettävyys** -välilehdessä sarakkeet, joita tarvitaan oikean verokoodin määrittämiseen, ja valitse sitten **Lisää**. Määritä tai valitse arvot kullekin sarakkeelle. **Nimikkeen veroryhmä** -kenttä on tämän matriisin tuotos. Jos tätä välilehteä ei määritetä, tapahtumarivin nimikkeen arvonlisäveroryhmää käytetään.

    Esimerkki:

    | Nimikekoodi | Nimikkeen veroryhmä |
    | --------- | -------------- |
    | D0001     | Täysi           |
    | D0003     | Vähennetty        |

    > [!NOTE]
    > Jos verotettavan nimikeasiakirjan rivien oletusarvoinen arvonlisäveroryhmä on oikein, jätä tämä matriisi tyhjäksi. Lisätietoja on myöhemmin tämän artikkelin [Suorituksenaikainen rakenne](#runtime) -osassa.

    Lisätietoja verokoodien määrittämisestä verolaskennassa on kohdassa [Arvolisäveroryhmän ja nimikkeen arvonlisäveroryhmän määrityslogiikka](global-sales-tax-group-determination.md).

24. Määritä asiakkaan verorekisteröintinumeroiden, toimittajien verorekisteröintinumeroiden ja luettelokoodien käytettävyydet liiketoimintatarpeiden perusteella.
25. Valitse **Tallenna** ja sulje sitten sivu.
26. Valitse **Muutoksen tila** \> **Viimeistele**. Kun tilaksi muutetaan **Valmis**, versiota ei voi enää muokata.
27. Valitse **Muuta tilaa** \> **Julkaise**. Tämä verotoiminnon asetusten versio työnnetään yleiseen tietovarastoon ja se näkyy kullekin Financen yritykselle.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Verolaskennan määrittäminen Dynamics 365:ssä

Kun RCS-määritykset on tehty, käytössä on verotoiminnon julkaistu versio. Näiden vaiheiden avulla voit määrittää verolaskennan Financessa.

Tämän osan määritykset tehdään yrityskohtaisesti. Se on määritettävä kullekin yritykselle, jolle verolaskenta otetaan käyttöön Financessa.

1. Valitse Financessa **Vero** \> **Asetukset** \> **Veromääritys** \> **Verolaskennan parametrit**.
2. Määritä **Yleiset**-välilehdessä seuraavat kentät:

    - **Ota verolaskentapalvelu käyttöön** – Verolaskentaa voidaan ottaa käyttöön yrityksessä valitsemalla tämä valintaruutu. Jos sitä ei ole otettu käyttöön nykyiselle yritykselle, yritys käyttää edelleen aiemmin luotua veromoduulia veron määrittämiseen ja laskemiseen.
    - **Ominaisuuden määritys** – Valitse yritykselle julkaistun verotoiminnon asetukset ja versio. Lisätietoja julkaistun verotoiminnon määrittämisestä ja suorittamisesta on tämän artikkelin edellisessä osassa.
    - **Liiketoimintaprosessi** – Valitse käyttöön otettavat liiketoimintaprosessit.

3. Määritä **Laskelma**-välilehdessä yrityksen odotettu pyöristyssääntö. Lisätietoja pyöristyslogiikasta on kohdassa [Verolaskennan pyöristyssäännöt](https://go.microsoft.com/fwlink/?linkid=2166988).
4. Määritä **Virheen käsittely** -välilehdessä yrityksen odotettu virheenkäsittelymenetelmä. Käytössä on kolme vaihtoehtoa:

    - Ei
    - Varoitus
    - Virhe

    Kunkin tuloskoodin virheiden käsittelymenetelmä määritetään **Tiedot**-osassa. Jos joitakin tuloskoodeja ei synkronoida verolaskentapalvelusta, oletusmenetelmä voidaan vaihtoehtoisesti määrittää **Yleiset**-osassa.

5. **Useita ALV-rekisteröintejä** -välilehdessä ALV-ilmoitus, EU:n arvonlisäveron yhteenvetoilmoitus ja Intrastat-ilmoitus voidaan ottaa erikseen käyttöön, jos kyse on useita ALV-rekisteröintejä käyttävästä skenaariosta. Lisätietoja useiden ALV-rekisteröintien veroilmoituksesta on kohdassa [Useiden ALV-rekisteröintien raportointi](emea-reporting-for-multiple-vat-registrations.md).
6. Tallenna määritykset ja toista edelliset vaiheet kunkin yrityksen kohdalla. Julkaistua uuttaa versiota voidaan käyttää tekemällä määritys **Verolaskennan parametrit** -sivun **Yleiset**-välilehden **Ominaisuuden asetus** -kentässä (katso vaihe 2).
