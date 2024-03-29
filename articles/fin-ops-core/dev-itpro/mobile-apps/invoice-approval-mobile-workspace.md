---
title: Laskujen hyväksyntöjen mobiilityötila
description: Tässä artikkelissa on tietoja laskujen hyväksyntöjen mobiilityötilasta.
author: abruer
ms.date: 05/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 4cc05d9fcea129cfb2ed8ed8df4bd4034a1fed4c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066387"
---
# <a name="invoice-approvals-mobile-workspace"></a>Laskujen hyväksyntöjen mobiilityötila

[!include [banner](../includes/banner.md)]
[!include [mobile app deprecation](../includes/mobile-app-deprecation-banner.md)]

Tässä artikkelissa on tietoja **laskujen hyväksyntöjen** mobiilityötilasta. Tässä työtilassa on luettelo laskuista, jotka on määritetty sinulle toimittajan laskun otsikon työnkulussa. 

Tämä mobiilityötila on tarkoitettu käytettäväksi talous- ja toimintosovellusten mobiilisovelluksen kanssa.

## <a name="overview"></a>Yleiskuvaus

**Laskun hyväksyntöjen** mobiilityötilan avulla ostoreskontran käsittelijät ja esimiehet voivat tarkastella laskuja, jotka on määritetty heille toimittajan laskun otsikon työnkulussa. Voit tarkastella laskun tietoja sekä rivi- ja jakelutietoja, mikä parantaa hyväksyntäpäätöksiä. Voit valita työtilassa toiminnon, jolla lasku siirtyy työnkulussa. 

## <a name="prerequisites"></a>Edellytykset

Mobiilityötilaa ei voi käyttää, ennen kuin seuraavat edellytykset ovat kunnossa.

<table>
<thead>
<tr class="header">
<th>Edellytys</th>
<th>Rooli</th>
<th>Kuvaus</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Microsoft Dynamics 365 Finance on otettava käyttöön organisaatiossa.</td>
<td>Järjestelmänvalvoja</td>
<td>Katso <a href="../deployment/deploy-demo-environment.md">Esittely-ympäristön käyttöönotto</a>.
</td>
</tr>
<tr class="even">
<td><strong>Laskun hyväksyntöjen</strong> mobiilityötila on julkaistava.</td>
<td>Järjestelmänvalvoja</td>
<td>Lisätietoja on ohjeaiheessa <a href="publish-mobile-workspace.md">Mobiilityötilan julkaiseminen</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>Mobiilisovelluksen lataaminen ja asentaminen

Talous- ja toimintosovelluksen mobiiliversion lataaminen ja asentaminen:

-   [Android-puhelimet](https://go.microsoft.com/fwlink/?linkid=850662)
-   [IPhone-puhelimet](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Kirjautuminen mobiilisovellukseen

1.  Käynnistä sovellus mobiililaitteessa.
2.  Anna Microsoft Dynamics 365:n URL-osoite.
3.  Käyttäjänimi ja salasana kysytään, kun kirjaudut sovellukseen ensimmäisen kerran. Kirjota tunnistetiedot.
4.  Kun olet kirjautunut sisään, yrityksen käytettävissä olevat työtilat ovat näkyvissä. Huomaa, että jos järjestelmänvalvoja julkaisee uuden työtilan myöhemmin, mobiilityötilojen luettelo on päivitettävä.

    [![Päivittäminen vetämällä.](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a>Laskun hyväksyminen laskun hyväksyntöjen mobiilityötilassa
1.  Valitse mobiililaitteessasi **laskun hyväksyntöjen** työtila.
2.  Valitse toimittajan laskun otsikon työnkulussa sinulle määritetty lasku.
3.  Tarkista **Laskun tiedot** -sivulla laskun otsikon tiedot, kuten toimittaja ja päivämäärä.
4.  Valitse laskurivi ja tarkastele sen yksityiskohtaisia tietoja **Laskurivin tiedot** -tietoja.
5.  Näytä rivijakelut valitsemalla **Laskurivin tiedot** -näkymässä **Jakelut**. Voit tarkastella täällä laskurivin kirjanpitoa. Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätili.
6.  Näytä kaikki jakelut valitsemalla **Laskun tiedot** -sivulla **Jakelut**. Voit tarkastella täällä koko lasku kirjanpitoa. Näitä tietoja ovat esimerkiksi taloushallinnon dimensiot ja päätilit. 
7.  Voit tarkastella laskuun liitettyjä huomautuksia tai tiedostoja valitsemalla **Liitteet**.
8.  Viimeistele tarkasteluprosessi valitsemalla **Laskun tiedot** -sivulla soveltuva työkulkutoiminto.
9.  Valitse **Valmis**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

