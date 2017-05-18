---
title: Dynamics 365 for Operations -mobiilisovelluksen kotisivu
description: "Tässä aiheessa kuvataan Microsoft Dynamics 365 mobiilisovellus ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi."
author: sericks007
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: e1a9e0eeb45f011ccb2aa091e68aff92782e1ae7
ms.contentlocale: fi-fi
ms.lasthandoff: 04/25/2017


---

# <a name="dynamics-365-for-operations-mobile-app-home-page"></a>Dynamics 365 for Operations -mobiilisovelluksen kotisivu

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]


Tässä aiheessa kuvataan Microsoft Dynamics 365 mobiilisovellus ja annetaan linkkejä resursseihin, jotka voivat auttaa sovellukseen käyttöönotossa organisaatiossasi.

<a name="overview"></a>Yleiskuvaus
--------

Microsoft Dynamics 365 for Operationsin mobiilisovellus mahdollistaa organisaatiosi liiketoimintaprosessien käytön mobiililaitteilla. Kun IT-järjestelmänvalvojasi ottaa mobiilityötilat käyttöön organisaatiossasi, käyttäjät voivat kirjautua sisään sovellukseen ja aloittaa liiketoimintaprosessien käyttämisen heti mobiililaitteillaan. Dynamics 365 for Operationsin mobiilisovellukseen sisältyvät seuraavat, tuottavuutta parantavat ominaisuudet:

-   Käyttäjät voivat tarkastella, muokata ja käynnistää toimita liiketoiminnan tiedoille, vaikka mobiililaitteen verkkoyhteys olisikin heikko tai laite offline-tilassa. Kun laitteen verkkoyhteys on jälleen käytössä, offline-tilassa tehdyt toimet synkronoidaan automaattisesti Dynamics 365 for Operationsiin.
-   IT-järjestelmänvalvojat tai sovelluskehittäjät voivat julkaista organisaatiolleen räätälöityjä mobiilityötiloja. Sovellus käyttää olemassa olevia koodiresursseja. Sinun ei siis täydy luoda tarkistusmenettelyitä, liiketoimintalogiikkaa tai suojausmäärittelyitä uudelleen.
-   IT-järjestelmänvalvoja tai sovelluskehittäjät voivat suunnitella mobiilityötiloja helposti Dynamics 365 for Operationsin verkkoasiakasohjelman työtilojen helppokäyttöisellä suunnitteluohjelmalla.
-   IT-järjestelmävalvojat voivat halutessaan optimoida työtilojen offline-ominaisuuksia liiketoimintalogiikan laajennuskehyksen avulla. Koska tietojen käsittely ei keskeydy laitteen ollessa offline-tilassa, mobiiliskenaariosi säilyvät mukautuvina, vaikka laitteilla ei olisikaan jatkuvaa verkkoyhteyttä.

## <a name="elements-of-the-mobile-app"></a>Mobiilisovelluksen osat
Mobiilisovelluksen käyttö koostuu neljästä, yksinkertaisesta osasta: koontinäyttö, työtilat, sivut ja toiminnot. 

[![Mobiilisovelluksen siirtymiskonseptit](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)

-   **Koontinäyttö** aukea, kun sovellus käynnistetään.
-   Koontinäytöllä näet luettelon **työtiloista**, jotka on julkaistu Dynamics 365 for Operations -ympäristössäsi.
-   Kussakin työtilassa näet luettelon **sivuista**, jotka ovat saatavilla kyseisessä työtilassa.
-   Sivuilla voit tarkastella tietoja, jotka on kerätty yhdestä tai useammasta Dynamics 365 for Operations -sivusta.
-   Sivuilta voit siirtyä muille sivuille, joilla on liittyviä tietoja, kuten yksikön tietoja tai rivejä.
-   Sivulla näet myös luettelon **toiminnoista**, jotka ovat saatavilla tälle sivulle.
-   Toimintojen avulla voit luoda tai muokata tietoja.

## <a name="implementation-process"></a>Käyttöönottoprosessi
Seuraavassa kuvassa esitellään Dynamics 365 for Operations -mobiilisovelluksen käyttöönoton prosessi organisaatiossa. 

[![](./media/mobile-implementation-process_4.png)](./media/mobile-implementation-process_4.png) 

Seuraava taulukko sisältää linkkejä resursseihin, jotka voivat auttaa Microsoft Dynamics 365 for Operations -mobiilisovelluksen käyttöönotossa organisaatiossasi. Ensimmäisen sarakkeen numerot vastaavat edellisessä kuvassa esitettyjä vaiheita.

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
<td>Suorita Dynamics 365 for Operationsin käyttöönotto organisaatiossa.</td>
<td>Jos organisaatiosi ei ole vielä ottanut Dynamics 365 for Operations -sovellusta käyttöön, tutustu <a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/deploy-demo-environment">Microsoft Dynamics 365 for Operations -kokeiluympäristön käyttöönotto</a>-ohjeeseen.</td>
</tr>
<tr class="even">
<td>2</td>
<td>Järjestelmänvalvoja</td>
<td>Lataa ja asenna paketit, jotka mahdollistavat Microsoftin tarjoamien mobiilityötilojen käytön.</td>
<td>Katso &quot;Edellytykset&quot; -osa sen mobiilityötilan ohjeesta, jota organisaatiosi haluaa käyttää:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Kustannusseurannan mobiilityötilat</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Käytettävissä olevan varaston mobiilityötila</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Myyntitilausten mobiilityötilat</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Toimittajayhteistyön mobiilityötila</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Projektin aikakirjausten mobiilityötila</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>3</td>
<td>Järjestelmänvalvoja</td>
<td>Julkaise Microsoftin tarjoamat mobiilityötilat.</td>
<td>Katso &quot;Edellytykset&quot; -osa sen mobiilityötilan ohjeesta, jota organisaatiosi haluaa käyttää:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Kustannusseurannan mobiilityötilat</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Käytettävissä olevan varaston mobiilityötila</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Myyntitilausten mobiilityötilat</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Toimittajayhteistyön mobiilityötila</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Projektin aikakirjausten mobiilityötila</a></li>
</ul></td>
</tr>
<tr class="even">
<td>4</td>
<td>Kehittäjä tai riippumaton ohjelmistotoimittaja (ISV)</td>
<td>Luo mukautettuja mobiilityötiloja Dynamics 365 for Operationsin mobiilikehyksen avulla.</td>
<td><ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform">Dynamics 365 for Operations -mobiilikehys</a></li>
<li><a href="http://ax.help.dynamics.com/en/wiki/operations-mobile-workspace-x-apis/">Dynamics 365 for Operationsin työtilojen X++ -sovellusohjelmaliittymät</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>5</td>
<td>riippumaton ohjelmistotoimittaja</td>
<td>Luo käyttöön otettava paketti, joka sisältää mukautettuja mobiilityötiloja ja lataa paketti Microsoft Dynamicsin elinkaaripalveluihin (LCS).</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/create-apply-deployable-package">Käyttöön otettavan paketin luominen</a></td>
</tr>
<tr class="even">
<td>6</td>
<td>Järjestelmänvalvoja</td>
<td>Avaa ohjelmistotoimittajan tarjoamat mukautetut työtilat sisältävä paketti.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/deployment/apply-deployable-package-system">Asenna käyttöön otettava paketti Microsoft Dynamics 365 for Operations -järjestelmään</a></td>
</tr>
<tr class="odd">
<td>7</td>
<td>Järjestelmänvalvoja</td>
<td>Julkaise ohjelmistotoimittajan tarjoamat, mukautetut mobiilityötilat.</td>
<td><a href="https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/mobile-apps/publish-mobile-workspace">Julkaise mobiilityötila</a></td>
</tr>
<tr class="even">
<td>8</td>
<td>Käyttäjä</td>
<td>Lataa ja asenna Dynamics 365 for Operations -mobiilisovellus.</td>
<td><ul>
<li>Android - <a href="https://play.google.com/store/apps/details?id=com.microsoft.dynamics365.operations.mobile">Dynamics 365 for Operations Google Play Storessa</a></li>
<li>iPhone - <a href="https://itunes.apple.com/us/app/dynamics-365-for-operations/id1180836730?mt=8">Dynamics 365 for Operations iTunes App Storessa</a></li>
</ul></td>
</tr>
<tr class="odd">
<td>9</td>
<td>Käyttäjä</td>
<td>Kirjaudu sisään ja käytä Dynamics 365 for Operations -mobiilisovellusta. Sovellus sisältää julkaistut mobiilityötilat.</td>
<td>Microsoftin toimittaa seuraavat mobiilityötilat:
<ul>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/cost-accounting/cost-controlling-mobile-workspace">Kustannusseurannan mobiilityötilat</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/inventory-on-hand-mobile-workspace">Käytettävissä olevan varaston mobiilityötila</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/production-control/sales-orders-mobile-workspace">Myyntitilausten mobiilityötilat</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/supply-chain/procurement/vendor-collaboration-mobile-workspace">Toimittajayhteistyön mobiilityötila</a></li>
<li><a href="https://docs.microsoft.com/en-us/dynamics365/operations/financials/project-management/project-time-entry-mobile-workspace">Projektin aikakirjausten mobiilityötila</a></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a>Lisätietoja
--------

[Dynamics 365 for Operations -mobiilisovellukselle julkaistut mobiilityötilat](mobile-workspaces-released.md)





