---
title: ER-mallien varmuuskopion tallennustila
description: Tässä ohjeaiheessa käsitellään tapaa, jolla malleja voi palauttaa sähköisen raportoinnin (ER) varmuuskopion tallennustilan avulla.
author: NickSelin
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8b4e783f79b02c77a27fc59c2f4be8a192f2f476
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248697"
---
# <a name="backup-storage-of-er-templates"></a>ER-mallien varmuuskopion tallennustila

[!include [banner](../includes/banner.md)]

Yrityskäyttäjät voivat määrittää [sähköisen raportoinnin (ER) kehyksen](general-electronic-reporting.md) avulla lähtevien asiakirjojen muodot eri maiden ja alueiden lakisääteisten vaatimusten mukaisiksi. Määritetyt ER-muodot voivat luoda valmiiksi määritettyjen mallien avulla erimuotoisia lähteviä asiakirjoja, kuten Microsoft Excel -työkirjoja, Microsoft Word -asiakirjoja tai PDF-tiedostoja. Malleihin täytetään ne tiedot, joita luotavia asiakirjoja varten määritetty tiedonkulku edellyttää.

Kukin määritetty muoto voidaan julkaista ER-ratkaisun osana. Kukin ER-ratkaisu voidaan viedä yhdestä Finance and Operationsin esiintymästä ja tuoda toiseen esiintymään.

ER-kehys säilyttää nykyisen Finance and Operations -esiintymän pakolliset mallit [tiedostojen hallintakehyksessä](../../fin-and-ops/organization-administration/configure-document-management.md). ER-kehyksen asetusten perusteella Microsoft Azure Blob Storage tai Microsoft SharePoint -kansio voidaan valita mallien ensisijaiseksi fyysiseksi tallennussijainniksi. (Lisätietoja on kohdassa [ER-kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md).) DocuValue-taulu sisältää kunkin mallin yksittäisen tietueen. Kunkin tietueen **AccessInformation**-kenttä sisältää määritetyssä tallennussijainnissa sijaitsevan mallitiedoston polun.

Finance and Operations -esiintymiä hallittaessa nykyinen esiintymä voidaan päättää siirtää toiseen sijaintiin. Voit esimerkiksi siirtää tuotantoesiintymän uuteen eristysympäristöön. Jos määrität ER-kehyksen tallentamaan mallit Blob-objektisäilöön, uuden eritysympäristön DocuValue-taulu viittaa tuotantoympäristön Blob-objektisäilöön. Tätä esiintymää ei kuitenkaan voi käyttää eristysympäristössä, koska siirtoprosessi ei tue artefaktien siirtoa Blob-objektisäilössä. Jos sitten yrität luoda liiketoiminta-asiakirjoja suorittamalla mallia käyttävän ER-muodon, tapahtuukin poikkeus ja saat ilmoituksen puuttuvasta mallista. Sinut myös ohjataan käyttämään ER-poistotyökalua sekä poistamaan ja tuomaan uudelleen mallin sisältävä ER-muodon määritys. Koska ER-muodon määrityksiä voi olla useita, tämä prosessi voi kestää kauan.

ER-mallien varmuuskopion tallennustilatoiminnon avulla voi olla mahdollista luoda mallit niin, että ne ovat aina käytettävissä liiketoiminta-asiakirjojen luontia varten.

> [!NOTE]
> Tätä toimintoa voi käyttää vain, jos Blob-objektisäilö on valittu ER-mallien fyysiseksi tallennussijainniksi.

Tätä toimintoa varten jokainen nykyisen ympäristön uusi ER-muodon määritys tallennetaan automaattisesti mallien varmuuskopion tallennussijaintiin (ERDocuDatabaseStorage-tietokantataulu) seuraavien tapahtumien yhteydessä:

- Uusi mallin sisältävä ER-muodon määritys tuodaan.
- Mallin sisältävän ER-muodon määrityksen luonnosversio viimeistellään.

Mallien varmuuskopiot siirretään uuteen Finance and Operations -esiintymään sovellustietokannan osana.

Jos ER-muodon malli tarvitaan esimerkiksi lähtevien asiakirjojen luontiin ja toimittajan maksujen käsittelyyn, mukaan lukien maksuilmoituksen ja valvontaraporttien luontiin, mutta tarvittavaa mallia ei löytynyt ensisijaisesta tallennussijainnista, tapahtuu seuraavaa:

- Jos malli on käytettävissä varmuuskopioinnin tallennussijainnissa, se haetaan automaattisesti sieltä ja palautetaan ensisijaiseen tallennussijaintiin, jonka jälkeen sitä voidaan käyttää nykyisessä toteutuksessa.
- Jokaiselle käyttäjälle, jolle on määritetty **Sähköisen raportoinnin kehittäjä**- tai **Järjestelmänvalvoja**-rooli, ilmoitetaan puuttuvasta mallista toimintokeskuksen kautta. Sanoman sisältö määräytyy **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametrin arvon mukaan:

    - Jos parametrin arvoksi on valittu **Ei käytössä**, sanoma suosittelee eräprosessin automaattista käynnistämistä, jotta vastaavat muiden ER-muodon määritysmallien ongelmat korjataan automaattisesti. Sanomassa on linkki, jolla eräprosessin voi aloittaa.
    - Jos parametrin arvoksi on valittu **Käytössä**, sanoma ilmoittaa, että puuttuvaan malliin liittyvä ongelma on havaittu ja että uusi eräprosessi **Palauta rikkoutuneet mallit sisäisestä tietokannan varmuuskopiosta** on ajoitettu automaattisesti. Tämä eräprosessi korjaa automaattisesti vastaavat ongelmat muissa malleissa.

Määritä **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametri seuraavasti:

1. Avaa Finance and Operationsissa **Organisaation hallinto \> Sähköinen raportointi \> Konfiguroinnit-sivu**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Käyttäjän parametrit** -valintaikkunassa tarvittava **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametrin arvo.

> [!NOTE]
> Tämä parametri määritetään sovelluksen käyttäjänä ja se on koskee sitä yritystä, johon on kirjauduttu.

![Sähköisen raportoinnin konfiguroinnit -sivu](./media/GER-BackupTemplates-1.png)

Seuraavassa kuvassa on esimerkki sanomasta, joka avautuu, kun **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametrin arvoksi on määritetty **Käytössä**.

![Toimittajan maksukirjauskansio -sivu](./media/GER-BackupTemplates-2.png)

Seuraavassa kuvassa on **Erätyö**-sivun **Palauta rikkoutuneet mallit sisäisestä tietokannan varmuuskopiosta** -eräprosessi.

![Erätyö-sivu](./media/GER-BackupTemplates-3.png)

Suoritetun **Palauta rikkoutuneet mallit sisäisestä tietokannan varmuuskopiosta** -eräprosessin suoritusloki sisältää tietoja malleista, jotka on palautettu varmuuskopion tallennussijainnista ensisijaiseen tallennussijaintiin.

![Erätyöhistoria-sivu](./media/GER-BackupTemplates-4.png)

ER-muodon määrityksessä olevien mallien automaattisen varmuuskopioiden luontiprosessi on oletusarvoisesti otettu käyttöön. Voit lopettaa mallin varmuuskopioinnin määrittämällä **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehdessä **Lopeta mallien varmuuskopiointi** -asetukseksi **Kyllä**. Voit avata sivun **Sähköinen raportointi** -työtilassa.

Jos määrität **Lopeta mallien varmuuskopiointi** -asetukseksi **Kyllä** etkä halua säilyttää malleista aiemmin tehtyjä varmuuskopioita, valitse **Tyhjennä varmuuskopioinnin tallennustila** **Sähköisen raportoinnin parametrit** -sivulla.

Jos päivität ympäristön Finance and Operationsin versioon 10.0.5 (lokakuu 2019) ja haluat siirtyä uuteen suoritettavia ER-muodon määrityksiä sisältävään ympäristöön, valitse **Täytä varmuuskopioinnin tallennustila** **Sähköisen raportoinnin parametrit** -sivulla ennen kuin siirto tehdään. Tämä painike aloittaa prosessin, jolla kaikki käytettävissä olevat mallit varmuuskopioidaan, jotta ne voidaan tallentaa mallien ER-varmuuskopioinnin tallennussijaintiin.

![Sähköisen raportoinnin parametrit -sivu](./media/GER-BackupTemplates-5.png)

## <a name="supported-deployments"></a>Tuetut käyttöönotot

Finance and Operationsin versiossa 10.0.5 ER-mallien varmuuskopioinnin tallennustila -toiminto on käytettävissä vain pilvikäyttöönotoissa.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportointikehyksen määrittäminen](electronic-reporting-er-configure-parameters.md)