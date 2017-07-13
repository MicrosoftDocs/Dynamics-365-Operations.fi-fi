---
title: "Laskujen hyväksyntöjen mobiilityötila"
description: "Tässä ohjeaiheessa on tietoja laskujen hyväksyntöjen mobiilityötilasta. Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 70f3e0fe53fc0b1daa471a7022f5659d09caa867
ms.contentlocale: fi-fi
ms.lasthandoff: 06/13/2017

---

# Laskujen hyväksyntöjen mobiilityötila
<a id="invoice-approvals-mobile-workspace" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja **laskujen hyväksyntöjen** mobiilityötilasta. Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa. 

Tätä mobiilityötilaa on tarkoitettu käytettäväksi Microsoft Dynamics 365 for Unified Operations -mobiilisovelluksella.

## Yleiskuvaus
<a id="overview" class="xliff"></a>

**Laskun hyväksyntöjen** mobiilityötilan avulla ostoreskontran käsittelijät ja esimiehet voivat tarkastella laskuja, jotka on määritetty heille toimittajan laskun otsikon työnkulussa. Voit tarkastella laskun tietoja sekä rivi- ja jakelutietoja, mikä parantaa hyväksyntäpäätöksiä. Voit valita työtilassa toiminnon, jolla lasku siirtyy työnkulussa. 

## Edellytykset
<a id="prerequisites" class="xliff"></a>

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
<td>Microsoft Dynamics 365 for Finance and Operations, Enterprise Editionin heinäkuun 2017 päivitys on oltava otettuna käyttöön organisaatiossa.</td>
<td>Järjestelmänvalvoja</td>
<td>Katso <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.
</td>
</tr>
<tr class="even">
<td><strong>Laskun hyväksyntöjen</strong> mobiilityötila on julkaistava.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## Mobiilisovelluksen lataaminen ja asentaminen
<a id="download-and-install-the-mobile-app" class="xliff"></a>

Lataa ja asenna Dynamics 365 for Unified Operations -mobiilisovellus:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## Kirjautuminen mobiilisovellukseen
<a id="sign-in-to-the-mobile-app" class="xliff"></a>

1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna oman Microsoft Dynamics 365:n URL-osoite.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

    [![Nouda päivitettäväksi](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## Laskun hyväksyminen laskun hyväksyntöjen mobiilityötilassa
<a id="approve-invoices-by-using-the-invoice-approvals-mobile-workspace" class="xliff"></a>
1.  Valitse mobiililaitteessasi **laskun hyväksyntöjen** työtila.
2.  Valitse toimittajan laskun otsikon työnkulussa sinulle määritetty lasku.
3.  Tarkista **Laskun tiedot** -sivulla laskun otsikon tiedot, kuten toimittaja ja päivämäärä.
4.  Valitse laskurivi ja tarkastele sen yksityiskohtaisia tietoja **Laskurivin tiedot** -tietoja.
5.  Näytä rivijakelut valitsemalla **Laskurivin tiedot** -näkymässä **Jakelut**. Voit tarkastella täällä laskurivin kirjanpitoa. Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätili.
6.  Näytä kaikki jakelut valitsemalla **Laskun tiedot** -sivulla **Jakelut**. Voit tarkastella täällä koko lasku kirjanpitoa. Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätilit. 
7.  Voit tarkastella laskuun liitettyjä huomautuksia tai tiedostoja valitsemalla **Liitteet**.
8.  Viimeistele tarkasteluprosessi valitsemalla **Laskun tiedot** -sivulla soveltuva työkulkutoiminto.
9.  Valitse **Valmis**.

