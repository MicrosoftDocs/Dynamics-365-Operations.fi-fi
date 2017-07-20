---
title: "Oman ryhmän mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja oman ryhmän mobiilityötilasta, jossa esimiehet voit tarkastella suoria alaisiaan ja laajennettua henkilökuntaa. Käyttäjät voivat myös lähettää kehuja raportointiketjuunsa kuuluville henkilöille."
author: ShielaSogge
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Talent, Operations, UnifiedOperations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 6178a9b1b5497672d68dee84a09800307ea60f54
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# <a name="my-team-mobile-workspace"></a>Oman ryhmän mobiilityötila

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **oman ryhmän** mobiilityötilasta. Esimiehet voivat tarkastella tässä työtilassa suoria alaisiaan ja laajennettua henkilökuntaa. He voivat myös lähettää kehuja raportointiketjuunsa kuuluville henkilöille.

Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.

## <a name="overview"></a>Yleiskuvaus 
Esimiehet voit tehdä seuraavia tehtäviä **oman ryhmän** mobiilityötilassa:

- Esimiehen suorista alaisista koostuvan luettelon tarkastelu.
- Esimiehen laajennetusta raportointiryhmästä koostuvan luettelon tarkastelu.
- Ryhmän kunkin jäsenen yksityiskohtaisten tietojen tarkastelu. Näitä tietoja ovat esimerkiksi syntymäaika, ikälisäpäivämäärä sekä kompensaatio- ja suoritustiedot.
- Kehun lähettäminen esimiehen laajennetun raportointiryhmän jäsenelle.

## <a name="prerequisites"></a>Edellytykset
Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.

<table>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Rooli</th>
<th>kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Organisaatiossa on oltava käytössä jokin seuraavista tuotteista:
<ul><li>Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys</li>
<li>Microsoft Dynamics 365 for Talent</li>
</ul>
</td>
<td>Järjestelmänvalvoja</td>
<td>Jos Finance and Operationsia ei ole vielä otettu organisaatiossa käyttöön, lisätietoja on ohjeaiheessa <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön ottaminen käyttöön</a>. Jos Talentia ei ole vielä otettu organisaatiossa käyttöön, järjestelmänvalvoja voi hakea kokeiluversion <a href="https://www.microsoft.com/en-us/dynamics365/talent">Talent-sivustosta</a>.
</td>
</tr>
<tr class="even">
<td><strong>Oman ryhmän</strong> mobiilityötila on julkaistava.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen

Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen
1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna oman Microsoft Dynamics 365:n URL-osoite.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

[![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a>Ryhmän jäsenten tarkastelu oman ryhmän mobiilityötilassa
1.  Valitse mobiilisovelluksessa **Oma ryhmä** -työtila. Luettelo ryhmän jäsenistä avautuu. Luettelossa on myös kunkin ryhmän jäsenen nimike sekä tämän mahdolliset suorat alaiset.
2.  Valitse ryhmän jäsen. **Ryhmän jäsenen yhteenveto** -sivu avautuu. Tällä sivulla olevia tietoja ovat esimerkiksi ryhmän jäsenen syntymäaika, ikälisäpäivä, vuodet nykyisessä toimessa ja kompensaation tiedot.

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a>Laajennetun ryhmän jäsenten tarkastelu oman ryhmän mobiilityötilassa
1.  Valitse mobiilisovelluksessa **Oma ryhmä** -työtila. Luettelo ryhmän jäsenistä avautuu. Luettelossa on myös kunkin ryhmän jäsenen nimike sekä tämän mahdolliset suorat alaiset.
1.  Valitse **Suorat alaiset** -linkki. Luettelo laajennetun ryhmän jäsenistä avautuu.
1.  Valitse ryhmän jäsen. **Ryhmän jäsenen yhteenveto** -sivu avautuu. Tällä sivulla olevia tietoja ovat esimerkiksi ryhmän jäsenen syntymäaika, ikälisäpäivä, vuodet nykyisessä toimessa ja kompensaation tiedot.

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a>Kehujen lähettäminen laajennetun ryhmän jäsenille oman ryhmän mobiilityötilassa
1.  Valitse mobiilisovelluksessa **Oma ryhmä** -työtila. Luettelo ryhmän jäsenistä avautuu. Luettelossa on myös kunkin ryhmän jäsenen nimike sekä tämän mahdolliset suorat alaiset.
1.  Valitse ryhmän jäsen. **Ryhmän jäsenen yhteenveto** -sivu avautuu.
1.  Valitse **Lähetä kehu**. 
1. Kirjoita kehu, jonka haluat lähettää. 
1. Valitse **Valmis**.
