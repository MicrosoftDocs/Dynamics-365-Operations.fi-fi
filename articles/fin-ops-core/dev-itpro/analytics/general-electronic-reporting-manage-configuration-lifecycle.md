---
title: Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta
description: Tässä artikkelissa kuvataan sähköisen raportoinnin konfiguraatioiden elinkaaren hallintaa Dynamics 365 Finance -ratkaisussa.
author: kfend
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: 0209679c9882d87edab68d043fba9e7b3400a2a2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337192"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan [sähköisen raportoinnin](general-electronic-reporting.md) [konfiguraatioiden](general-electronic-reporting.md#Configuration) elinkaaren hallintaa Dynamics 365 Finance -ratkaisussa.

## <a name="overview"></a>Yleiskuvaus

Sähköinen raportointi on moduuli, joka tukee lakisääteisiä ja maakohtaisia sähköisten asiakirjojen vaatimuksia. Sähköisessä raportoinnissa oletuksena on se, että yksittäisille sähköisille asiakirjoille voidaan suorittaa seuraavat tehtävät. Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) yleiskuvaus](general-electronic-reporting.md).

- Sähköisen asiakirjan malli suunnitteleminen:

    - Tunnista vaaditut tietolähteet, jotka voidaan esittää asiakirjassa:

        - Taustatiedot, kuten tietotaulukot, tietoyksiköt ja luokat.
        - Prosessikohtaiset ominaisuudet (suorituspäivämäärä ja -aika sekä aikavyöhyke).
        - Käyttäjän syöttöparametrit (loppukäyttäjä määrittää suorituksen aikana).

    - Määrittele asiakirjassa tarvittavat osat ja niiden topologia, jotta voit määrittää asiakirjalle lopullisen muodon.
    - Määritä haluamasi valituista tietolähteistä tuleva tietovirta määriteltyihin asiakirjan elementteihin (sitomalla tietolähteet asiakirjan muotokomponentteihin) ja määritä prosessinhallintalogiikka.

- Julkaise malli käyttöön niin, että sitä voidaan käyttää muissa esiintymissä:

    - Muunna luotu asiakirjamalli sähköisen raportoinnin konfiguraatioon ja vie se nykyisestä sovellusesiintymästä XML-pakettina, joka voidaan tallentaa joko paikallisesti tai Lifecycle Servicesiin (LCS).
    - Muunna sähköisen raportoinnin konfiguraatio sovelluksen asiakirjamalliksi.
    - Tuo XML-paketti, joka tallennetaan paikallisesti tai LCS:ään nykyiseen esiintymään.

- Mukauta sähköisen asiakirjan mallia:

    - Tuo malli sähköisen raportoinnin konfiguraationa LCS:stä nykyiseen esiintymään.
    - Suunnittele sähköisen raportoinnin konfiguraatiosta mukautettu versio, mutta säilytä viittaus perusversioon.

- Integroi malli tiettyyn liiketoimintaprosessiin niin, että se on käytettävissä sovelluksessa:

    - Määritä asetukset siten, että sovellus alkaa käyttää sähköisen raportoinnin konfiguraatiota, viittaamalla kyseiseen konfiguraatioon prosessiin liittyvällä parametrilla. Voit esimerkiksi viitata sähköisen raportoinnin konfiguraatioon tietyssä ostoreskontran maksumenetelmässä, jos haluat luoda sähköisen maksuviestin laskujen käsittelyä varten.

- Käytä mallia määrätyssä liiketoimintaprosessissa:

    - Suorita sähköisen raportoinnin konfiguraatio määrätyssä liiketoimintaprosessissa. Voit esimerkiksi viitata sähköisen raportoinnin konfiguraatioon tietyssä ostoreskontran maksumenetelmässä, jos haluat luoda sähköisen maksuviestin laskujen käsittelyä varten.

## <a name="concepts"></a>Käsitteet
Sähköisen raportoinnin konfiguraatioiden elinkaareen liittyvät seuraavat roolit ja tehtävät.

| Rooli                                       | Tehtävät                                                      | kuvaus |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| Sähköisen raportoinnin toiminnallinen konsultti | Sähköisen raportoinnin komponenttien (mallien ja muotojen) luonti ja hallinta.           | Yrityksessä työskentelevä henkilö, joka suunnittelee sähköisen raportoinnin toimialuekohtaisia tietomalleja, suunnittelee sähköisissä asiakirjoissa tarvittavat mallit ja liittää ne vastaavasti. |
| Sähköisen raportoinnin kehittäjä             | Tietomallien yhdistämismääritysten luonti ja hallinta.                          | Asiantuntija, joka valitsee tarvittavat Finance-tietolähteet ja sitoo ne sähköisen raportoinnin toimialuekohtaisiin tietomalleihin. |
| Taloushallintopäällikkö                      | Sähköisen raportoinnin artefakteihin viittaavien prosessiin liittyvien asetusten määrittäminen. | Esimerkiksi **Taloushallintopäällikkö**-rooli, joka sallii sähköisen raportoinnin konfiguraation asetusten käyttämisen tietyssä ostoreskontran maksumenetelmässä sähköisen maksuviestin luomiseksi laskujen käsittelyä varten. |
| Ostoreskontran maksuliikenneassistentti            | Sähköisen raportoinnin artefaktien käyttäminen määrätyssä liiketoimintaprosessissa.                | Esimerkiksi **Ostoreskontran maksuliikenneassistentti** -rooli, joka sallii sähköisten maksuviestien luomisen laskujen käsittelyä varten tietylle maksutavalle määritetyn sähköisen raportoinnin muodon perusteella. |

## <a name="er-configuration-development-lifecycle"></a>Sähköisen raportoinnin konfiguraation kehityksen elinkaari
On suositeltavaa, että sähköisen raportoinnin konfiguraatiot suunnitellaan kehitysympäristössä erillisenä talous- ja toimintosovellusten esiintymänä seuraavista sähköiseen raportointiin liittyvistä syistä:

- Käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat muokata konfiguraatioita ja suorittaa ne sitten testitarkoituksissa. Tämä skenaario saattaa aiheuttaa kutsuja luokkien tai taulujen menetelmistä, jotka voivat olla vahingollisia liiketoimintatiedoille ja esiintymän suorituskyvylle.
- Aloituskohdat ja kirjattu yrityksen sisältö eivät rajoita luokkien ja taulujen menetelmien kutsuja sähköisen raportoinnin tietolähteinä tai konfiguraatioina. Niinpä käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat päästä käsiksi salassa pidettäviin tietoihin.

Kehitysympäristössä suunnitellut sähköisen raportoinnin konfiguraatiot voidaan [ladata](#data-persistence-consideration) testiympäristöön konfiguraation arviointia (oikea prosessi-integraatio, tulosten oikeellisuus, suorituskyky) ja laadunvarmistusta (roolipohjaisten käyttöoikeuksien oikeellisuus, tehtävien eriyttäminen jne.) varten. Tähän tarkoitukseen voidaan käyttää toimintoja, jotka sallivat sähköisen raportoinnin konfiguraatioiden vaihdon. Testatut sähköisen raportoinnin konfiguraatiot voidaan ladata joko LCS:ään, jakaa palvelun tilaajille, tai [tuoda](#data-persistence-consideration) tuotantoympäristöön sisäiseen käyttöön.

![ER-konfiguraation elinkaari.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Tietojen pysyvyyden huomioon ottaminen

Voit yksitellen [tuoda](tasks/er-import-configuration-lifecycle-services.md) ER-[määrityksen](general-electronic-reporting.md#Configuration) eri versioita Finance-esiintymään. Kun tuot uuden ER-konfiguraation version, järjestelmä ohjaa tämän konfiguraation luonnosversion sisältöä:

- Kun tuotu versio on pienempi kuin nykyisen taloustietoinstanssin tämän konfiguraation ylin versio, tämän konfiguraation luonnosversion sisältö pysyy muuttumattomana.
- Kun tuotu versio on suurempi kuin mikään muu tämän konfiguroinnin versio nykyisessä taloustietoinstanssissa, tuodun version sisältö kopioidaan tämän konfiguraation luonnosversioon, jotta voit jatkaa viimeisen valmiin version muokkausta.

Jos tämän konfiguraation [omistaa](general-electronic-reporting.md#Provider) tällä hetkellä aktivoitu konfiguraatiopalvelu, konfiguraation luonnosversio näkyy konfiguroinnit-sivun **Versiot**-pikavälilehdillä **Määritykset**-sivulla (**Organisaation hallinta** > **Sähköinen raportointi** > **Määritykset**). Voit valita konfiguraation luonnosversion ja [muokata](er-quick-start2-customize-report.md#ConfigureDerivedFormat) sen sisältöä käyttämällä ER-suunnittelutoimintoa. Kun olet muokannut ER-kokoonpanon luonnosversiota, sen sisältö ei enää vastaa tämän kokoonpanon korkeimman version sisältöä nykyisessä Finance-ilmentymässä. Jos haluat estää muutosten menettämisen, järjestelmä näyttää virheen, jota tuonti ei voi jatkua, koska tämän konfiguraation versio on suurempi kuin nykyisen taloustietoinstanssin tämän konfiguraation korkein versio. Jos esimerkiksi muodon määritys on **X**, **muodon X-versio ei ole valmis** -virhe ilmestyy näkyviin.

Voit peruuttaa luonnosversiossa tekemäsi muutokset valitsemalla ER-konfiguraation suurimman valmiin tai jaetun version **Versiot**-pikavälilehdissä ja valitsemalla sitten **Hae tämä versio**  -vaihtoehdon. Valitun version sisältö kopioidaan luonnosversioon.

## <a name="applicability-consideration"></a>Soveltuvuudessa huomioonotettavaa

Kun ER-määrityksen uusi versio suunnitellaan, sen [riippuvuus](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) muihin ohjelmiston osiin voidaan määrittää. Tämä vaihe on edellytys tämän määrityksen version sähköisen raportoinnin säilöstä tai ulkoisesta XML-tiedostosta latauksen hallinnan ja muiden tämän version käyttötarkoitusten edellytys. Kun ER-määrityksen uusi versio yritetään tuoda, järjestelmä hallitsee version tuontia määritettyjen edellytysten avulla.

Joissakin tapauksissa saatetaan edellyttää, että järjestelmä ohittaa määritetyn edellytykset ER-määritysten uusia versioita tuotaessa. Järjestelmä saadaan ohittamaan edellytykset tuonnin aikana seuraavasti:

1. Valitse **Organisaation hallinto** \> **Sähköinen raportointi** \> **Konfiguraatiot**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Ohita tuotepäivitykset ja version edellytystarkistus tuonnin aikana** -asetukseksi **Kyllä**.

    > [!NOTE]
    > Tämä parametri on käyttäjä- ja yrityskohtainen.

## <a name="dependencies-on-other-components"></a>Muiden komponenttien riippuvuudet

ER-konfiguraatiot voidaan määrittää [riippuvaisiksi](er-download-configurations-global-repo.md#import-filtered-configurations) muista konfiguraatioista. Voit esimerkiksi [tuoda](er-download-configurations-global-repo.md) ER-[tietomallin](er-overview-components.md#data-model-component) konfiguraation yleisestä tietovarastosta [Microsoft Regulatory Configuration Servicesiin (RCS)](../../../finance/localizations/rcs-overview.md) tai Dynamics 365 Finance -instanssiin ja luoda sitten uuden ER-[muoto](er-overview-components.md#format-component)konfiguraation, joka [johdetaan](er-quick-start2-customize-report.md#DeriveProvidedFormat) tuodusta ER-tietomallin konfiguroinnista. Johdettu ER-muotomääritys on riippuvainen ER-perustietomallin konfiguraatiosta.

![Johdettu ER-muodon määritys Määritykset-sivulla.](./media/ger-configuration-lifecycle-img1.png)

Kun olet lopettanut muodon määrittämisen, voit muuttaa ER-muodon määrityksen alkuperäisen version tilan **Luonnos** tilaksi **Valmis**. Sen jälkeen voit jakaa ER-muotokonfiguraation valmiin version [julkaisemalla](../../../finance/localizations/rcs-global-repo-upload.md) sen yleisessä tietovarastossa. Seuraavaksi voit käyttää yleistä tietovarastoa mistä tahansa RCS:n tai Financen pilviesiintymästä. Tämän jälkeen voit tuoda minkä tahansa sovellukseen sovellettavan ER-konfiguraatioversion yleisestä tietovarastosta kyseiseen sovellukseen.

![Julkaistu ER-muotomääritys konfiguraation tietovarasto -sivulla.](./media/ger-configuration-lifecycle-img2.png)

Määrityksen riippuvuuden perusteella kun valitset yleisestä tietovarastosta ER-muotokonfiguraation tuomista varten uuteen RCS:n tai Financen esiintymään, ER-tietomallin peruskonfiguraatio löytyy automaattisesti yleisestä tietovarastosta ja se tuodaan yhdessä valitun ER-muodon konfiguraation kanssa peruskonfiguraationa.

Voit myös viedä ER-muotoisen konfigurointiversion nykyisestä RCS:n tai Financen esiintymästä ja tallentaa sen paikallisesti XML-tiedostona.

![ER-muodon konfiguraatioversion vieminen XML-muotoon konfigurointisivulla.](./media/ger-configuration-lifecycle-img3.png)

Financen versioissa **ennen versiota 10.0.29**, kun yrität tuoda ER-muotokonfiguraatioversion XML-tiedostosta tai mistä tahansa muusta tietovarastosta kuin yleisestä tietovarastosta vastikään käyttöön otettuun RCS:n tai Financen esiintymään, joka ei vielä sisällä ER-konfiguraatioita, seuraava poikkeus ilmenee kertoen, ettei peruskonfiguraatiota voi saada:

> Selvittämättömiä viitteitä jäljellä<br>
Objektin \<imported configuration name\> viittausta objektiin 'Perus' (\<globally unique identifier of the missed base configuration\>, \<version of the missed base configuration\>) ei voi muodostaa

![ER-muodon konfiguraatioversion tuominen konfiguraation tietovarasto -sivulla.](./media/ger-configuration-lifecycle-img4.gif)

Jos yrität tuoda samaa konfiguraatiota **versiossa 10.0.29 ja sitä uudemmassa versiossa**, jos peruskonfiguraatiota ei löydy nykyisestä sovellusesiintymästä tai lähdetietovarastosta, joka on käytössä (soveltuvin osin), ER-kehys yrittää automaattisesti etsiä puuttuvan peruskonfiguraation nimen yleisen tietovaraston välimuistista. Sen jälkeen se esittää puuttuvan peruskonfiguraation nimen ja GUID-tunnuksen annettavan poikkeuksen tekstissä.

> Selvittämättömiä viitteitä jäljellä<br>
Objektin \<imported configuration name\> viittausta objektiin 'Perus' (\<name of the missed base configuration\> \<globally unique identifier of the missed base configuration\>, \<version of the missed base configuration\>) ei voi muodostaa

![Poikkeus konfigurointitietovarastosivulla, kun peruskonfiguraatiota ei löydy.](./media/ger-configuration-lifecycle-img5.png)

Voit etsiä peruskonfiguraation käyttämällä annettua nimeä ja tuoda sen sitten manuaalisesti.

> [!NOTE]
> Tämä uusi vaihtoehto toimii vain , jos vähintään yksi käyttäjä on jo kirjautunut yleiseen tietovarastoon käyttämällä [Konfiguraatiosäilöt](er-download-configurations-global-repo.md#open-configurations-repository)-sivua tai yhtä nykyisen Finance-esiintymän yleisen tietovaraston [hakukenttää](er-extended-format-lookup.md) ja kun yleisen tietovaraston sisältö on tallennettu välimuistiin.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin konfiguraatioiden riippuvuuden määrittäminen muissa komponenteissa](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

