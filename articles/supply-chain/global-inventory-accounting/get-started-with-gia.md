---
title: Yleisen varastokirjanpidon käytön aloittaminen
description: Tässä aiheessa kuvataan, kuinka yleinen varastokirjanpito otetaan käyttöön.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cfba2b8320399cc2eb3f2231e8a172d902633f16
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678856"
---
# <a name="get-started-with-global-inventory-accounting"></a>Yleisen varastokirjanpidon käytön aloittaminen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)] <!--KFM: Until 4/30/2022 -->

Yleisen varastokirjanpidon avulla voit suorittaa useita varastokirjanpitoja määrittämissäsi yleisissä varastokirjanpitorekistereissä. Kukin yleinen varastokirjanpitotapahtuma liitetään *käytäntöön*. Yleissopimus on kokoelma seuraavantyyppisiä kirjanpitokäytäntöjä:

- Kustannusobjekti
- Syötteen mittaperuste
- Kustannusvirran oletus
- Kustannustaso

> [!NOTE]
> Vaikka olet ottanut yleisen varastokirjanpidon käyttöön, voit silti tehdä varastokirjanpidon Microsoft Dynamics 365 Supply Chain Management -ohjelmassa tavalliseen tapaan.

Yleinen varastokirjanpito on apuohjelma. Jos haluat käyttää sen toimintoja, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesistä (LCS). Voit valita, että se arvioidaan testiympäristössä, ennen kuin otat sen käyttöön tuotantoympäristöissä.

Yleinen varastolaskenta ei tällä hetkellä tue kaikkia Supply Chain Managementiin integroituja kustannustenhallintaominaisuuksia. Tämän vuoksi on tärkeää arvioida, vastaako tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.

## <a name="how-to-get-the-global-inventory-accounting-public-preview"></a><a name="sign-up"></a>Yleisen varastolaskennan julkisen esiversion saaminen

> [!IMPORTANT]
> Jotta voit käyttää yleistä varastokirjanpitoa, sinulla on oltava LCS-yhteensopiva korkean käytettävyyden ympäristö (ei OneBox-ympäristö). Lisäksi käytössä tulee olla Supply Chain Managementin versio 10.0.19 tai sitä myöhempi.

Jos haluat rekisteröityä yleisen varastokirjanpidon julkiseen esiversioon, lähetä LCS-ympäristötunnus sähköpostitse [yleiselle varastokirjanpitotiimille](mailto:GlobalInvAccount@microsoft.com). Kun olet hyväksynyt ohjelman, tiimi lähettää sinulle seurantasähköpostiviestin, joka sisältää yleisen varastokirjanpidon beta-avaimen ja huollon päätepisteet. Kun olet saanut beta-avaimen, [voit asentaa lisäosan](#install).

## <a name="licensing"></a>Käyttöoikeudet

Yleinen varastokirjanpito on lisensoitu yhdessä Supply Chain Managementin käytettävissä olevien varastokirjanpidon vakiotoimintojen kanssa. Sinun ei tarvitse ostaa lisäkäyttöoikeutta, jotta voisit käyttää yleistä varastokirjanpitoa.

## <a name="prerequisites"></a>Edellytykset

### <a name="set-up-microsoft-power-platform-integration"></a>Määritä Microsoft Power Platform -integroinnin asetukset

Ennen kuin voit ottaa apuohjelmatoiminnon käyttöön, sinun on integroitava Microsoft Power Platformiin noudattamalla seuraavia vaiheita.

1. Avaa LCS-ympäristö, johon haluat lisätä palvelun.
1. Valitse **Kaikki tiedot**.
1. Valitse **Määritys** **Power Platform -integrointi** -osasta.
1. Valitse valintaruutu **Power platform -ympäristön asetus** -valintaikkunassa ja valitse sitten **Asetukset**. Asetusten määritys kestää yleensä 60 - 90 minuuttia.
1. Kun Microsoft Power Platform -ympäristö on tehty valmiiksi, sivulla näkyy ympäristösi nimi. **Power Platform -Integrointi** -osassa näkyy myös lauseke "Power Platform -ympäristöasetukset on tehty". Yleinen varastokirjanpito ei edellytä kaksoiskirjoitussovellusta.

Lisätietoja on ohjeaiheessa [Salliminen ympäristön käyttöönoton jälkeen](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md#enable-after-deploy).

### <a name="set-up-dataverse"></a>Määritä Dataverse

Lisää yleiset varastokirjanpidon palveluperiaatteet vuokraajaasi ennen Dataversen käyttöä seuraavasti:

1. Asenna Azure AD Module for Windows PowerShell v2, kuten kuvattu kohdassa [Asenna Azure Active Directory PowerShell for Graph](/powershell/azure/active-directory/install-adv2).
1. Suorita seuraava PowerShell-komento.

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)

    New-AzureADServicePrincipal -AppId "7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9" -DisplayName "d365-scm-costaccountingservice"

    New-AzureADServicePrincipal -AppId "5f58fc56-0202-49a8-ac9e-0946b049718b" -DisplayName "d365-scm-operationdataservice"
    ```

Luo seuraavaksi sovelluskäyttäjät yleistä varastokirjanpitoa varten Dataversessä noudattamalla seuraavia ohjeita.

1. Avaa Dataverse-ympäristön URL-osoite.
1. Valitse **Lisäasetukset \> Järjestelmä \> Suojaus \> Käyttäjät** ja luo sovelluskäyttäjä. Vaihda sivunäkymäksi *Sovelluskäyttäjät* **Näkymä**-valikossa.
1. Valitse **Uusi**.
1. Määritä **Sovellustunnus**-kentän arvoksi *7a1dd80f-c961-4a67-a2f5-d6a5d2f52cf9*.
1. Valitse **Määritä rooli** ja valitse sitten *Järjestelmänvalvoja*. Jos saatavana on rooli nimeltä *Common Data Service -käyttäjä*, valitse myös se.
1. Toista edelliset vaiheet, mutta määritä **Sovellustunnus**-kentän arvoksi *5f58fc56-0202-49a8-ac9e-0946b049718b*.

Lisätietoja on kohdassa [Sovelluskäyttäjän luominen](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user).

Jos Dataverse-asennuksen oletuskieli ei ole englanti, noudata seuraavia ohjeita.

1. Siirry kohtaan **Lisäasetukset \> Hallinta \> Kielet**.
1. Valitse *englanti* (*LanguageCode=1033*) ja valitse **Ota käyttöön**.

## <a name="install-the-add-in"></a><a name="install"></a>Lisäosan asentaminen

Asenna lisäosa noudattamalla seuraavia ohjeita, jotta voit käyttää yleistä varastokirjanpitoa.

1. [Kirjaudu](#sign-up) yleisen varastolaskennan julkisen esiversioon.
1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index).
1. Mene kohtaan **Toimintojen hallinnan esiversio**.
1. Valitse plusmerkki (**+**).
1. Syötä **Koodi**-kenttään yleisen varastokirjanpidon apuohjelman beeta-avain. (Sinun olisi pitänyt saada beeta-avain sähköpostitse rekisteröityessäsi.)
1. Valitse **Poista esto**.
1. Avaa LCS-ympäristö, johon haluat lisätä palvelun.
1. Valitse **Kaikki tiedot**.
1. Siirry **Power Platform -integrointiin** ja valitse **Asetukset**.
1. Valitse valintaruutu **Power platform -ympäristön asetus** -valintaikkunassa ja valitse sitten **Asetukset**. Asetusten määritys kestää yleensä 60 - 90 minuuttia.
1. Kun Microsoft Power Platform -ympäristö on tehty valmiiksi, valitse **Ympäristö-lisäosat**-pikavälilehdillä **Asenna uusi lisäosa**.
1. Valitse **Yleinen varastokirjanpito**.
1. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.
1. Valitse **Asenna**.
1. **Ympäristön apuohjelmat** -pikavälilehdessä näkyy, että yleistä varastokirjanpitoa asennetaan. Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta *Asennetaan* tilaan *Asennettu*. (Sivu on ehkä päivitettävä, jotta näet tämän muutoksen.) Tässä vaiheessa yleinen varastokirjanpito on valmis käytettäväksi.

## <a name="set-up-the-integration"></a>Määritä integraatio

Seuraavia ohjeita noudattamalla voit määrittää yleisen varastokirjanpidon ja Supply Chain Managementin integroinnin.

1. Kirjaudu Supply Chain Managementiin.
1. Siirry kohtaan **Järjestelmänhallinta \> Ominaisuuksien hallinta**.
1. Valitse **Tarkista päivitysten saatavuus**.
1. Etsi **Kaikki**-välilehdestä toiminto, jonka nimi on *Yleinen varastokirjanpito*.
1. Valitse **Ota käyttöön nyt**.
1. Siirry kohtaan **Yleinen varastokirjanpito \> Asetukset \> Yleisen varastokirjanpidon parametrit \> Integrointi-parametrit**.
1. Kirjoita **Tietopalvelun päätepiste**- ja **Yleisen varastokirjanpidon päätepiste** -kenttiin sen sähköpostiviestin URL-osoitteet, jonka yleinen varastokirjanpitotiimi on lähettänyt rekisteröityessäsi esiversioon.

Yleinen varastokirjanpito on nyt valmis käytettäväksi.
