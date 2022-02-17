---
title: Yleinen vianmääritys
description: Tässä ohjeaiheessa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista taloushallinnon ja toimintojen sovellusten ja Dataversen välillä.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6f5b9f26990e2f4db9bf69040a6c4be31400b40
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062335"
---
# <a name="general-troubleshooting"></a>Yleinen vianmääritys

[!include [banner](../../includes/banner.md)]



Tässä ohjeaiheessa on yleisiä vianetsintätietoja kaksoiskirjoituksen integroinnista taloushallinnon ja toimintojen sovellusten ja Dataversen välillä.

> [!IMPORTANT]
> Jotkin tämän ohjeaiheen osoitteet saattavat edellyttää joko järjestelmänvalvojan roolia tai Microsoftin Azure Active Directory (Azure AD) -vuokralaisen järjestelmänvalvojan valtuuksia. Kussakin osassa selitetään, tarvitaanko tiettyä roolia tai tunnistetietoja.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Ota käyttöön laajennuksena toimiva jäljitysloki Dataversessä virheen tietojen tarkastelemiseksi

**Jäljityslokin ottaminen käyttöön ja virheiden tarkasteleminen:** järjestelmän hallintarooli

Jäljitysloki otetaan käyttöön seuraavasti.

1. Kirjaudu asiakasvuorovaikutussovellukseen, avaa **Asetukset**-sivu ja valitse sitten **Järjestelmä**-kohdasta **Hallinta**.
2. Valitse **Hallinta**-sivulla **Järjestelmäasetukset**.
3. Ota laajennuksen jäljitysloki käyttöön valitsemalla **Mukauttaminen**-välilehden **Laajennuksen ja mukautetun työnkulun tehtävän jäljitys**-sarakkeessa **Kaikki**. Jos haluat kirjata jäljityslokit vain, kun poikkeuksia ilmenee, voit valita kohdan **Poikkeus** sen sijaan.


Jäljitysloki näytetään seuraavasti.

1. Kirjaudu asiakasvuorovaikutussovellukseen, avaa **Asetukset**-sivu ja valitse sitten **Mukautus**-kohdasta **Laajennuksen jäljitysloki**.
2. Etsi jäljityslokit, joiden **Tyyppinimi**-sarakkeen arvoksi on määritetty **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Voit tarkastella koko lokia kaksoisnapsauttamalla kohdetta ja tarkistaa sitten **Suoritus**-pikavälilehdessä **Sanomalohko**-tekstin.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Virheenkorjaustilan käyttöönotto taloushallinnon ja toimintojen sovellusten live-synkronointiongelmien vianmäärityksessä

**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja

Sovellukseen perustuvat kaksoiskirjoitusvirheet Dataversessä voivat näkyä taloushallinnon ja toimintojen sovelluksessa. Virheiden sanatarkka kirjaaminen otetaan käyttöön seuraavasti:

1. Kaikissa taloushallinnon ja toimintojen sovelluksen projektimäärityksessä on **IsDebugMode**-merkintä **DualWriteProjectConfiguration**-taulukossa.
2. Avaa **DualWriteProjectConfiguration** käyttämällä Excel-apuohjelmaa. Apuohjelman käyttöä varten on otettava käyttöön suunnittelutila taloushallinnon ja toimintojen sovelluksen Excel-apuohjelmassa ja lisättävä **DualWriteProjectConfiguration** taulukkoon. Lisätietoja on kohdassa [Yksikön tietojen näyttäminen ja päivittäminen Excelissä](../../office-integration/use-excel-add-in.md).
3. Määritä projekti **IsDebugMode**-asetukseksi **Kyllä**.
4. Suorita virheitä tuottava skenaario.
5. Sanatarkat lokit tallennetaan **DualWriteErrorLog**-taulukossa.
6. Taulukon tietoja haetaan käyttämällä selaimessa linkkiä `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` ja korvaamalla `999` tarvittaessa.
7. Päivitys tehdään uudelleen päivityksen [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe) jälkeen, ja se on saatavana platform update 37- ja sen jälkeisissä päivityksissä. Jos tämä korjaus on asennettu, virheenkorjaustilalla siepataan lisää lokeja.Jos olet asentanut tämän korjauksen, virheenkorjaustila kerää enemmän lokeja.  

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Taloushallinnon ja toimintojen sovelluksen virtuaalikoneen synkronointivirheiden tarkistaminen

**Virheiden tarkastelemiseen tarvittava rooli:** Järjestelmänvalvoja

1. Kirjaudu Microsoft Dynamics Lifecycle Servicesiin (LCS).
2. Avaa LCS-projekti, jonka valitsit kaksoiskirjoitustestauksen suorittamista varten.
3. Valitse **Pilvipalveluympäristöt**-ruutu.
4. Voit kirjautua taloushallinnon ja toimintojen sovelluksen virtuaalikoneeseen (VM) etätyöpöydän avulla. Käytä LCS:ssä näkyvää paikallista tiliä.
5. Avaa tapahtumien katseluohjelma.
6. Valitse **Sovellusten ja palveluiden lokit \> Microsoft \> Dynamics \> AX -DualWriteSync \> Toiminnassa**.
7. Tarkista viimeaikaisten virheiden luettelo.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Toisen Dataverse -ympäristön linkityksen poistaminen ja linkittäminen taloushallinnon ja toimintojen sovelluksesta

**Ympäristön linkityksen poistamiseen vaadittu rooli:** Joko taloushallinnon ja toimintojen sovelluksen tai Dataversen järjestelmänvalvoja.

1. Kirjaudu taloushallinnon ja toimintojen sovellus.
2. Siirry kohtaan **Työtilat \> Tietojen hallinta** ja valitse **Kaksoiskirjoitus**-ruutu.
3. Valitse kaikki käynnissä olevat yhdistämismääritykset ja valitse sitten **Pysäytä**.
4. Valitse **Poista ympäristön linkitys**.
5. Vahvista toiminto valitsemalla **Kyllä**.

Nyt voit linkittää uuden ympäristön.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Myyntitilausrivin tietolomaketta ei voi tarkastella 

Kun luot myyntitilauksen Dynamics 365 Salesissa, + **Lisää tuotteet** -vaihtoehdon napsauttaminen saattaa ohjata sinut Dynamics 365 Project Operationsin tilausrivilomakkeeseen. Kyseisessä lomakkeessa ei ole mitään tapaa tarkastella myyntitilausrivin **Tieto**-lomaketta. **Tietoja**-vaihtoehto ei näy **Uuden tilausrivin** alla olevassa avattavassa valikossa. Näin tapahtuu, koska Project Operations on asennettu ympäristöösi.

Voit ottaa **Tieto**-lomakevaihtoehdon uudelleen käyttöön seuraavasti:

1. Siirry **Tilausrivi**-taulukkoon.
2. Etsi **Tieto**-lomake lomakkeet-solmussa.
3. Valitse **Tieto**-lomake ja valitse **Ota käyttöön käyttöoikeusroolit**.
4. Muuta suojausasetukseksi **Näytä kaikille**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Verkkojäljityksen ottaminen käyttöön ja tallentaminen siten, että jäljitys voidaan liittää tukipalvelupyyntöihin

Tukitiimin on ehkä tarkistettava verkkojäljitykset ongelmien vianmääritystä varten. Verkkoseuranta luodaan seuraavasti:

### <a name="chrome"></a>Chrome

1. Avaa kehittäjän työkalut painamalla avoimessa välilehdessä **F12**-näppäintä tai valitsemalla **Kehittäjän työkalut**.
2. Avaa **Verkko**-välilehti ja kirjoita **integ** suodatinruutuun.
3. Suorita skenaario ja tarkkaile lokiin kirjattavia pyyntöjä.
4. Napsauta merkintöjä hiiren kakkospainikkeella ja valitse **Tallenna kaikki HAR-tiedostona, jossa on sisältöä**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Avaa kehittäjän työkalut painamalla avoimessa välilehdessä **F12**-näppäintä tai valitsemalla **Kehittäjän työkalut**.
2. Avaa **Verkko**-välilehti.
3. Suorita skenaario.
4. Vie tulokset HAR-tiedostona valitsemalla **tallenna**.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
