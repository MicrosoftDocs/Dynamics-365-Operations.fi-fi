---
title: Mobiilisovelluksen aloitussivu
description: Tässä ohjeaiheessa käsitellään Finance and Operations (Dynamics 365) -mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.
author: sericks007
manager: AnnBe
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 012b51b66c831a66a54c7c868735e310f05eb8c1
ms.sourcegitcommit: f939bc6292840e29bc0f498efc8f4641dfe8f994
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/22/2020
ms.locfileid: "2975194"
---
# <a name="mobile-app-home-page"></a>Mobiilisovelluksen aloitussivu

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään **Finance and Operations (Dynamics 365)** -mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.

<a name="overview"></a>Yleiskuvaus
--------

Mobiilisovelluksen avulla organisaatiosi liiketoimintaprosesseja voi käyttää mobiililaitteilla. Kun IT-järjestelmänvalvoja ottaa mobiilityötilat käyttöön organisaatiossa, käyttäjät voivat kirjautua sisään sovellukseen ja aloittaa liiketoimintaprosessien käyttämisen heti mobiililaitteillaan. Mobiilisovellukseen sisältyvät seuraavat, tuottavuutta parantavat ominaisuudet:

- Käyttäjät voivat tarkastella, muokata ja käynnistää toimita liiketoiminnan tiedoille, vaikka mobiililaitteen verkkoyhteys olisikin heikko tai laite offline-tilassa. Kun laitteen verkkoyhteys on jälleen käytössä, offline-tilassa tehdyt toimet synkronoidaan automaattisesti.
- IT-järjestelmänvalvojat tai sovelluskehittäjät voivat julkaista organisaatiolleen räätälöityjä mobiilityötiloja. Sovellus käyttää olemassa olevia koodiresursseja. Sinun ei siis täydy luoda tarkistusmenettelyitä, liiketoimintalogiikkaa tai suojausmäärittelyitä uudelleen.
- IT-järjestelmänvalvoja tai sovelluskehittäjät voivat suunnitella mobiilityötiloja helposti verkkoasiakasohjelman työtilojen helppokäyttöisellä suunnitteluohjelmalla.
- IT-järjestelmävalvojat voivat halutessaan optimoida työtilojen offline-ominaisuuksia liiketoimintalogiikan laajennuskehyksen avulla. Koska tietojen käsittely ei keskeydy laitteen ollessa offline-tilassa, mobiiliskenaariosi säilyvät mukautuvina, vaikka laitteilla ei olisikaan jatkuvaa verkkoyhteyttä.

## <a name="elements-of-the-mobile-app"></a>Mobiilisovelluksen osat
Mobiilisovelluksen käyttö koostuu neljästä, perusosasta: koontinäyttö, työtilat, sivut ja toiminnot. 

[![Mobiilisovelluksen siirtymiskonseptit](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

1. **Koontinäyttö** aukea, kun sovellus käynnistetään.
2. Koontinäytössä on luettelo julkaistuista **työtiloista**.
3. Kussakin työtilassa näet luettelon **sivuista**, jotka ovat saatavilla kyseisessä työtilassa.
4. Kun olet sivulla, voit suorittaa siellä useita toimintoja. Seuraavassa on muutamia esimerkkejä:

    - Yksityiskohtaisten tietojen tarkastelu.
    - Siirtyminen muille sivuille, joilla on liittyviä tietoja, kuten yksikön tietoja tai rivejä.
    - Tutustu luetteloon **toiminnoista**, jotka ovat käytettävissä kyseiseltä sivulta. Toimintojen avulla voit luoda tai muokata tietoja.

## <a name="implementation-process"></a>Käyttöönottoprosessi
Seuraavassa kuvassa on esitys Microsoftin toimittamien mobiilityötilojen ja mukautettujen mobiilityötilojen käyttöönottamisesta. 

[![Mobiilisovellusten käyttöönottoprosessi](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)

Seuraavassa taulukossa on linkkejä resursseihin, jotka auttavat ottamaan käyttöön sekä Microsoftin tarjoamia mobiilityötiloja että mukautettuja mobiilityötiloja. Ensimmäisen sarakkeen numerot vastaavat edellisessä kuvassa esitettyjä vaiheita.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Vaihe</th>
<th>Rooli</th>
<th>Toimenpide</th>
<th>Resursseja, jotka auttavat suorittamaan toiminnon</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>1</td>
<td>Järjestelmänvalvoja</td>
<td>Ota Finance and Operations -sovellus käyttöön organisaatiossasi.</td>
<td><ul><li>Jos et ole vielä ottanut Microsoft Dynamics 365 -versiota käyttöön, lisätietoja on kohdassa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</li><li>Jos haluat tutustua käytettävissä oleviin mobiilityötilaluetteloihin, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Järjestelmänvalvoja</td>
<td><strong>Jos käytössä on Microsoft Dynamics 365 for Operationsin versio 1611:</strong> Lataa ja asenna paketit, jotka mahdollistavat Microsoftin tarjoamien mobiilityötilojen käytön.</td>
<td>Lisätietoja on seuraavissa ohjeaiheissa:
<ul>

<li><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Kustannusseurannan mobiilityötilat</a></li>
<li><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Käytettävissä olevan varaston mobiilityötila</a></li>
<li><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Myyntitilausten mobiilityötilat</a></li>
<li><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Toimittajayhteistyön mobiilityötila</a></li>
<li><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Projektin aikamerkintöjen mobiilityötila</a></li>
<li><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Kulujen hallinnan mobiilityötila</a></li>

</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Järjestelmänvalvoja</td>
<td>Julkaise Microsoftin tarjoamat mobiilityötilat.</td>
<td><a href="publish-mobile-workspace.md">Julkaise mobiilityötila</a>
</td>
</tr>
<tr class="even">
<td>4</td>
<td>Kehittäjä tai riippumaton ohjelmistotoimittaja (ISV)</td>
<td>Luo mukautettuja mobiilityötiloja mobiiliympäristön avulla.</td>
<td><a href="platform/mobile-platform-home-page.md">Mobiiliympäristö</a></td>
</tr>
<tr class="odd">
<td>5</td>
<td>riippumaton ohjelmistotoimittaja</td>
<td>Luo käyttöön otettava paketti, joka sisältää mukautettuja mobiilityötiloja ja lataa paketti Microsoft Dynamics Lifecycle Services (LCS) -palveluun.</td>
<td><a href="../deployment/create-apply-deployable-package.md">Käyttöönotettavan paketin luominen</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Järjestelmänvalvoja</td>
<td>Avaa riippumattoman ohjelmistotoimittajan tarjoamat mukautetut työtilat sisältävä paketti.</td>
<td><a href="../deployment/apply-deployable-package-system.md">Käyttöönotettavan paketin käyttäminen</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Järjestelmänvalvoja</td>
<td>Julkaise ohjelmistotoimittajan tarjoamat, mukautetut mobiilityötilat.</td>
<td><a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Käyttäjä</td>
<td>Lataa ja asenna mobiilisovellus.</td>
<td>
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations -sovellus Androidille</a><BR/>
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations -sovellus iOSille</a><BR/>
(Windows Phonea ei tueta)
</td>
</tr>
<tr class="odd">
<td>9</td>
<td>Käyttäjä</td>
<td>Kirjaudu mobiilisovellukseen ja käytä sitä. Sovellus sisältää järjestelmänvalvojan julkaisemat mobiilityötilat.</td>
<td>Jos haluat tutustua Microsoftin toimittamaan mobiilityötilaluetteloon, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a>Vianmääritys
[Mobiiliympäristön resurssit](platform/mobile-platform-home-page.md#troubleshooting-the-app)
