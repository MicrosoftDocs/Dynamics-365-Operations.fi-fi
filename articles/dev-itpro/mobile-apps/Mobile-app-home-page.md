---
title: Mobiilisovelluksen kotisivu
description: "Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Unified Operationsin mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 233d91138b11905d971be90154da54e61bbe2919
ms.contentlocale: fi-fi
ms.lasthandoff: 12/01/2017

---

# <a name="mobile-app-home-page"></a>Mobiilisovelluksen kotisivu

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Unified Operationsin mobiilisovellusta ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.

> [!NOTE]
> Mobiilisovelluksen nimi oli aiemmin *Microsoft Dynamics 365 for Finance and Operations*.

<a name="overview"></a>Yleiskuvaus
--------

Mobiilisovelluksen avulla organisaatiosi liiketoimintaprosesseja voi käyttää mobiililaitteilla. Kun IT-järjestelmänvalvoja ottaa mobiilityötilat käyttöön organisaatiossa, käyttäjät voivat kirjautua sisään sovellukseen ja aloittaa liiketoimintaprosessien käyttämisen heti mobiililaitteillaan. Mobiilisovellukseen sisältyvät seuraavat, tuottavuutta parantavat ominaisuudet:

- Käyttäjät voivat tarkastella, muokata ja käynnistää toimita liiketoiminnan tiedoille, vaikka mobiililaitteen verkkoyhteys olisikin heikko tai laite offline-tilassa. Kun laite muodostaa verkkoyhteyden uudelleen, offline-tietotoiminnot synkronoidaan automaattisesti Dynamics 365 for Finance and Operations, Enterprise Editionin tai Microsoft Dynamics 365 for Finance and Operationsin kanssa.
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

![Mobiilisovellusten käyttöönottoprosessi](./media/Mobile-implementation-process-5.png)

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
<td>Ota Finance and Operations käyttöön organisaatiossasi</td>
<td><ul><li>Jos et ole vielä ottanut Microsoft Dynamics 365 -versiosta, lisätietoja on ohjeaiheessa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.</li><li>Jos haluat tutustua käytettävissä oleviin mobiilityötilaluetteloihin, lisätietoja on ohjeaiheessa <a href="mobile-workspaces-released.md">Äskettäin vapautetut mobiilityötilat</a>.</li></ul></td>
</tr>
<tr class="even">
<td>2</td>
<td>Järjestelmänvalvoja</td>
<td><strong>Jos käytössä on Microsoft Dynamics 365 for Finance and Operationsin versio 1611:</strong> Lataa ja asenna KB:t, joilla otetaan Microsoftin mobiilityötilat käyttöön.</td>
<td>Lisätietoja on seuraavissa ohjeaiheissa:
<ul>

<li><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Kustannusseurannan mobiilityötilat</a></li>
<li><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Käytettävissä olevan varaston mobiilityötila</a></li>
<li><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Myyntitilausten mobiilityötilat</a></li>
<li><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Toimittajayhteistyön mobiilityötila</a></li>
<li><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Projektin aikamerkintöjen mobiilityötila</a></li>
<li><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Kulujen hallinnan mobiilityötila</a></li>

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
<td><a href="../deployment/create-apply-deployable-package.md">Käyttöön otettavan paketin luominen</a></td>
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
<td><a href="publish-mobile-workspace.md">Mobiilityötilan julkaisu</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Käyttäjä</td>
<td>Lataa ja asenna mobiilisovellus.</td>
<td><ul>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android-puhelimet</a></li>
<li><a href="https://go.microsoft.com/fwlink/?linkid=850663">IPhone-puhelimet</a></li></ul>
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

