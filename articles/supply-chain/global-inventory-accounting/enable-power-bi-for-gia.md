---
title: Power BI:n ottaminen käyttöön yleisessä varastokirjanpidossa
description: Tässä artikkelissa kuvataan, kuinka Microsoft Power BI otetaan käyttöön yleisessä varastokirjanpidossa.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b1edfa314d2810bff4cf02762aeb66bee801858d
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135422"
---
# <a name="enable-power-bi-for-global-inventory-accounting"></a>Power BI:n ottaminen käyttöön yleisessä varastokirjanpidossa

[!include [banner](../includes/banner.md)]

Voit kiinnittää ruutuja, koontinäyttöjä ja raportteja [PowerBI.com](https://powerbi.com/)-tilitäsi Microsoft Dynamics 365 -sovelluksen työtilaan.

## <a name="prerequisites"></a>Edellytykset

Seuraavien edellytysten on oltava käytössä, ennen kuin voit ottaa Power BI -raportoinnin käyttöön:

- Sinun tulee olla Dynamics 365 -sovelluksen järjestelmänvalvoja.
- Sinulla on oltava [PowerBI.com](https://powerbi.com/)-tili.
- Tililläsi on oltava vähintään yksi koontinäyttö ja yksi raportti Power BI -tililläsi.
- Vain oman Azure Active Directory (Azure AD) -tilisi järjestelmänvalvoja.
- Azure AD -toimialueen on oltava sama toimialue, jota käytät [PowerBI.com](https://powerbi.com/)-tilissäsi.

## <a name="setup"></a>Luo perustiedot

Määritä Power BI -integrointi noudattamalla näitä ohjeita.

1. Kirjaudu [Microsoft Dynamics Lifecycle Servicesiin (LCS)](https://lcs.dynamics.com/Logon/Index).
1. Siirry **Jaettuun resurssikirjastoon**, valitse **Power BI -raporttimalli** resurssin tyypiksi ja lataa **Yleinen varastokirjanpito**. 
1. Kirjaudu sisään [PowerBI.comiin](https://app.powerbi.com/) ja lataa **Yleisen varastokirjanpidon** Power BI -raporttitiedosto noudattamalla seuraavia vaiheita:

    1. Valitse **Uusi**.
    1. Valitse **Lataa tiedosto palveluun**.
    1. Valitse **Yleisen varastokirjanpidon** Power BI -raporttitiedosto.

1. Konfiguroi **Yleisen varastokirjanpidon** Power BI -raportti seuraavien vaiheiden mukaisesti:

    1. Siirry kohtaan **Oma työtila**, etsi yleisen varastokirjanpidon tietojoukko ja valitse **Asetukset** **Asetukset**-valikosta.
    1. Laajenna **Yleisen varastokirjanpidon asetukset** -kohdassa **Parametrit** ja päivitä kaikki parametrit tarpeen mukaan. Varmista erityisesti seuraavat asetukset:
        1. Korvaa **Dataverse-URL**-oletusarvot käyttäen **Power platform -ympäristön tiedot** -sivulla olevia arvoja LCS:n (**Power platform-integroinnin** osassa).
        1. Korvaa **Ympäristötunnus**-oletusarvot käyttäen LCS:n **Ympäristötiedot**-kohdassa olevia arvoja (**Ympäristön hallinta** -osiossa).
        1. Valitse **Tietolähteen tunnistetiedot** -osassa Olevan **CDS**-otsikon vieressä oleva **Muokkaa tunnistetietoja** -linkki. Kirjaudu sitten Dataverse-tilillesi **OAuth2**-todennusmenetelmällä.
    1. Tarkista, että Power BI -raportit kohdassa **Oma työtila \> Raportit \> Yleinen varastolaskenta** toimivat oikein ja näyttävät järjestelmän sisältöä.

1. Rekisteröi sovellus [Määritä PowerBI.com-integrointi](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md#registration-process) -kohdassa kuvatulla tavalla.
1. Integroi **Yleisen varastokirjanpidon** Power BI -raporttitiedosto Dynamics 365 Supply Chain Managementiin seuraavien vaiheiden mukaisesti:

    1. Valitse **Järjestelmän hallinta \> Asetukset \> PowerBI.comin konfiguraatio**.
    1. Valitse **Muokkaa**.
    1. Valitse **Ota käyttöön PowerBI.Com -integrointi**.
    1. Syötä **Sovellustunnus**-kenttään sovellustunnus.
    1. Syötä **Sovellusavain**-kenttään sovellusavain.
    1. Valitse **Tallenna**.

1. Päivitä sivu, jotta Power BIn kirjautumisvalintaikkuna tulee näkyviin.
1. Valitse **Asetukset**-välilehdestä **Avaa raporttiluettelo** ja valitse sitten aiemmin lataamasi **Yleisen varastokirjanpidon** Power BI -raporttitiedosto.
1. Päivitä sivu. Näin voit nähdä, että raporttisi on lisätty.
1. Valitse **Power BI -raportit** kohdasta **Yleinen varastokirjanpito** -linkki.

Lisätietoja kohdasta [Konfiguroi PowerBI.com-integraatiosi](../../fin-ops-core/dev-itpro/analytics/configure-power-bi-integration.md).
