---
title: Sähköisen raportoinnin mallien varmuuskopion tallennustila
description: Tässä artikkelissa käsitellään tapaa, jolla malleja voi palauttaa sähköisen raportoinnin (ER) varmuuskopion tallennustilan avulla.
author: kfend
ms.date: 04/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-08-13
ms.dyn365.ops.version: 10.0.5
ms.custom: 27621
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable
ms.openlocfilehash: 61e6119c50ee79d8623d1b49d273fb8c07f88944
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281899"
---
# <a name="backup-storage-of-er-templates"></a>ER-mallien varmuuskopion tallennustila

[!include [banner](../includes/banner.md)]

Yrityskäyttäjät voivat määrittää [sähköisen raportoinnin (ER) yleiskatsauksen](general-electronic-reporting.md) avulla lähtevien asiakirjojen muodot eri maiden ja alueiden lakisääteisten vaatimusten mukaisiksi. Määritetyt ER-muodot voivat luoda valmiiksi määritettyjen mallien avulla erimuotoisia lähteviä asiakirjoja, kuten Microsoft Excel -työkirjoja, Microsoft Word -asiakirjoja tai PDF-tiedostoja. Malleihin täytetään ne tiedot, joita luotavia asiakirjoja varten määritetty tiedonkulku edellyttää.

Kukin määritetty muoto voidaan julkaista ER-ratkaisun osana. Kukin ER-ratkaisu voidaan viedä yhdestä talous- ja toimintosovellusesiintymästä ja tuoda toiseen esiintymään.

ER-kehys säilyttää nykyisen talous- ja toimintosovellusesiintymän pakolliset mallit [tiedostojen hallinnan määrityksen](../../fin-ops/organization-administration/configure-document-management.md) avulla. ER-kehyksen asetusten perusteella Microsoft Azure Blob Storage tai Microsoft SharePoint -kansio voidaan valita mallien ensisijaiseksi fyysiseksi tallennussijainniksi. (Lisätietoja on kohdassa [Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md).) DocuValue-taulu sisältää kunkin mallin yksittäisen tietueen. Kunkin tietueen **AccessInformation**-kenttä sisältää määritetyssä tallennussijainnissa sijaitsevan mallitiedoston polun.

Talous- ja toimintosovellusesiintymiä hallittaessa nykyinen esiintymä voidaan päättää siirtää toiseen sijaintiin. Voit esimerkiksi siirtää tuotantoesiintymän uuteen eristysympäristöön. Jos määrität ER-kehyksen tallentamaan mallit Blob-objektisäilöön, uuden eritysympäristön DocuValue-taulu viittaa tuotantoympäristön Blob-objektisäilöön. Tätä esiintymää ei kuitenkaan voi käyttää eristysympäristössä, koska siirtoprosessi ei tue artefaktien siirtoa Blob-objektisäilössä. Jos sitten yrität luoda liiketoiminta-asiakirjoja suorittamalla mallia käyttävän ER-muodon, tapahtuukin poikkeus ja saat ilmoituksen puuttuvasta mallista. Sinut myös ohjataan käyttämään ER-poistotyökalua sekä poistamaan ja tuomaan uudelleen mallin sisältävä ER-muodon määritys. Koska ER-muodon määrityksiä voi olla useita, tämä prosessi voi kestää kauan.

ER-mallien varmuuskopion tallennustilatoiminnon avulla voi olla mahdollista luoda mallit niin, että ne ovat aina käytettävissä liiketoiminta-asiakirjojen luontia varten.

> [!NOTE]
> Tätä toimintoa voi käyttää vain, jos Blob-objektisäilö on valittu ER-mallien fyysiseksi tallennussijainniksi.

## <a name="automated-recovery-and-notification"></a>Automatisoitu palautus ja ilmoitus

Tätä toimintoa varten jokainen nykyisen ympäristön uusi ER-muodon määritys tallennetaan automaattisesti mallien varmuuskopion tallennussijaintiin (ERDocuDatabaseStorage-tietokantataulu) seuraavien tapahtumien yhteydessä:

- Uusi mallin sisältävä ER-muodon määritys tuodaan.
- Mallin sisältävän ER-muodon määrityksen luonnosversio viimeistellään.

Mallien varmuuskopiot siirretään uuteen talous- ja toimintosovellusesiintymään sovellustietokannan osana.

Jos ER-muodon malli tarvitaan esimerkiksi lähtevien asiakirjojen luontiin ja toimittajan maksujen käsittelyyn, mukaan lukien maksuilmoituksen ja valvontaraporttien luontiin, mutta tarvittavaa mallia ei löytynyt ensisijaisesta tallennussijainnista, tapahtuu seuraavaa:

- Jos malli on käytettävissä varmuuskopioinnin tallennussijainnissa, se haetaan automaattisesti sieltä ja palautetaan ensisijaiseen tallennussijaintiin, jonka jälkeen sitä voidaan käyttää nykyisessä toteutuksessa.
- Jokaiselle käyttäjälle, jolle on määritetty **Sähköisen raportoinnin kehittäjä**- tai **Järjestelmänvalvoja**-rooli, ilmoitetaan puuttuvasta mallista toimintokeskuksen kautta. Sanoman sisältö määräytyy **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametrin arvon mukaan:

    - Jos parametrin arvoksi on valittu **Ei käytössä**, sanoma suosittelee eräprosessin automaattista käynnistämistä, jotta vastaavat muiden ER-muodon määritysmallien ongelmat korjataan automaattisesti. Sanomassa on linkki, jolla eräprosessin voi aloittaa.
    - Jos parametrin arvoksi on valittu **Käytössä**, sanoma ilmoittaa, että puuttuvaan malliin liittyvä ongelma on havaittu ja että uusi eräprosessi **Palauta rikkoutuneet mallit sisäisestä tietokannan varmuuskopiosta** on ajoitettu automaattisesti. Tämä eräprosessi korjaa automaattisesti vastaavat ongelmat muissa malleissa.

Määritä **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametri seuraavasti:

1. Avaa talous- ja toimintosovelluksissa **Organisaation hallinto \> Sähköinen raportointi \> Määritykset-sivu**.
2. Valitse **Määritykset**-sivun toimintoruudun **Määritykset**-välilehden **Lisämääritykset**-ryhmässä **Käyttäjäparametrit**.
3. Määritä **Käyttäjän parametrit** -valintaikkunassa tarvittava **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametrin arvo.

> [!NOTE]
> Tämä parametri määritetään sovelluksen käyttäjänä ja se on koskee sitä yritystä, johon on kirjauduttu.

![Sähköisen raportoinnin konfiguroinnit -sivu.](./media/GER-BackupTemplates-1.png)

Seuraavassa kuvassa on esimerkki sanomasta, joka avautuu, kun **Suorita rikkoutuneiden mallien palautusmenettely automaattisesi eränä** -parametrin arvoksi on määritetty **Käytössä**.

![Toimittajan maksukirjauskansio -sivu.](./media/GER-BackupTemplates-2.png)

Seuraavassa kuvassa on **Erätyö**-sivun **Palauta rikkoutuneet mallit sisäisestä tietokannan varmuuskopiosta** -eräprosessi.

![Erätyö-sivu.](./media/GER-BackupTemplates-3.png)

Suoritetun **Palauta rikkoutuneet mallit sisäisestä tietokannan varmuuskopiosta** -eräprosessin suoritusloki sisältää tietoja malleista, jotka on palautettu varmuuskopion tallennussijainnista ensisijaiseen tallennussijaintiin.

![Erätyöhistoria-sivu.](./media/GER-BackupTemplates-4.png)

ER-muodon määrityksessä olevien mallien automaattisen varmuuskopioiden luontiprosessi on oletusarvoisesti otettu käyttöön. Voit lopettaa mallin varmuuskopioinnin määrittämällä **Sähköisen raportoinnin parametrit** -sivun **Liitteet**-välilehdessä **Lopeta mallien varmuuskopiointi** -asetukseksi **Kyllä**. Voit avata sivun **Sähköinen raportointi** -työtilassa.

Jos määrität **Lopeta mallien varmuuskopiointi** -asetukseksi **Kyllä** etkä halua säilyttää malleista aiemmin tehtyjä varmuuskopioita, valitse **Tyhjennä varmuuskopioinnin tallennustila** **Sähköisen raportoinnin parametrit** -sivulla.

Jos päivität ympäristön talous- ja toimintosovellusten versioon 10.0.5 (lokakuu 2019) ja haluat siirtyä uuteen suoritettavia ER-muodon määrityksiä sisältävään ympäristöön, valitse **Täytä varmuuskopioinnin tallennustila** **Sähköisen raportoinnin parametrit** -sivulla ennen kuin siirto tehdään. Tämä painike aloittaa prosessin, jolla kaikki käytettävissä olevat mallit varmuuskopioidaan, jotta ne voidaan tallentaa mallien ER-varmuuskopioinnin tallennussijaintiin.

![Sähköisen raportoinnin parametrit -sivu.](./media/GER-BackupTemplates-5.png)

## <a name="manual-recovery"></a>Manuaalinen palautus

Siirry kohtaan **Organisaation hallinta** \> **Sähköinen raportointi** \> **Palauta rikkinäiset mallit** -toiminto, joka käynnistää manuaalisesti ER-mallien palautusprosessin varmuuskopion tallennuspaikasta ensisijaiselle tallennuspaikalle. Ennen tämän prosessin aloittamista **Palauta rikkinäiset mallit** -sivulla voit määrittää, suoritetaanko se vuorovaikutteisesti vai ajoitetaanko eräkäsittely.

## <a name="supported-deployments"></a>Tuetut käyttöönotot

Talous- ja toimintosovellusten versiossa 10.0.5 ER-mallien varmuuskopioinnin tallennustila -toiminto on käytettävissä vain pilvikäyttöönotoissa.

## <a name="additional-resources"></a>Lisäresurssit

[Sähköisen raportoinnin (ER) yleiskatsaus](general-electronic-reporting.md)

[Sähköisen raportoinnin (ER) kehyksen määrittäminen](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
