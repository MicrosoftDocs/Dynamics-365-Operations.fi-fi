---
title: Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta
description: Tässä artikkelissa kuvataan sähköisen raportoinnin konfiguraatioiden elinkaaren hallintaa Dynamics 365 Finance -ratkaisussa.
author: NickSelin
ms.date: 07/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0220fa03283119471b3d1f78a23a04ed4036264e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906794"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a>Sähköisen raportoinnin (ER) määritysten elinkaaren hallinta

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan sähköisen raportoinnin konfiguraatioiden elinkaaren hallintaa Dynamics 365 Finance -ratkaisussa.

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
On suositeltavaa, että sähköisen raportoinnin konfiguraatiot suunnitellaan kehitysympäristössä erillisenä Finance and Operations -esiintymänä seuraavista sähköiseen raportointiin liittyvistä syistä:

- Käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat muokata konfiguraatioita ja suorittaa ne sitten testitarkoituksissa. Tämä skenaario saattaa aiheuttaa kutsuja luokkien tai taulujen menetelmistä, jotka voivat olla vahingollisia liiketoimintatiedoille ja esiintymän suorituskyvylle.
- Aloituskohdat ja kirjattu yrityksen sisältö eivät rajoita luokkien ja taulujen menetelmien kutsuja sähköisen raportoinnin tietolähteinä tai konfiguraatioina. Niinpä käyttäjät, joilla on joko **Sähköisen raportoinnin kehittäjä**- tai **Sähköisen raportoinnin toiminnallinen konsultti** -rooli, voivat päästä käsiksi salassa pidettäviin tietoihin.

Kehitysympäristössä suunnitellut sähköisen raportoinnin konfiguraatiot voidaan [ladata](#data-persistence-consideration) testiympäristöön konfiguraation arviointia (oikea prosessi-integraatio, tulosten oikeellisuus, suorituskyky) ja laadunvarmistusta (roolipohjaisten käyttöoikeuksien oikeellisuus, tehtävien eriyttäminen jne.) varten. Tähän tarkoitukseen voidaan käyttää toimintoja, jotka sallivat sähköisen raportoinnin konfiguraatioiden vaihdon. Testatut sähköisen raportoinnin konfiguraatiot voidaan ladata joko LCS:ään, jakaa palvelun tilaajille, tai [tuoda](#data-persistence-consideration) tuotantoympäristöön sisäiseen käyttöön.

![ER-konfiguraation elinkaari.](./media/ger-configuration-lifecycle.png)

## <a name="data-persistence-consideration"></a>Tietojen pysyvyyden huomioon ottaminen

Voit [tuoda](tasks/er-import-configuration-lifecycle-services.md) eri [versioita](general-electronic-reporting.md#component-versioning) ER-[konfiguraatiosta](general-electronic-reporting.md#Configuration) yksitellen Finance-instanssiisi. Kun tuot uuden ER-konfiguraation version, järjestelmä ohjaa tämän konfiguraation luonnosversion sisältöä:

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

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin konfiguraatioiden riippuvuuden määrittäminen muissa komponenteissa](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
