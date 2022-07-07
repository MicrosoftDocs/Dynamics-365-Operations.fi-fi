---
title: Yleisen varastokirjanpidon käytön aloittaminen
description: Tässä artikkelissa kuvataan, kuinka yleinen varastokirjanpito otetaan käyttöön.
author: JennySong-SH
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: cbe6bff6fab96900b8bd4e112a8858363fff86d1
ms.sourcegitcommit: 9870b773a2ea8f5675651199fdbc63ca7a1b4453
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/15/2022
ms.locfileid: "9013552"
---
# <a name="get-started-with-global-inventory-accounting"></a>Yleisen varastokirjanpidon käytön aloittaminen

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!--KFM: Preview until 4/30/2022 -->

Yleisen varastokirjanpidon avulla voit suorittaa useita varastokirjanpitoja määrittämissäsi yleisissä varastokirjanpitorekistereissä. Kukin yleinen varastokirjanpitotapahtuma liitetään *käytäntöön*. Yleissopimus on kokoelma seuraavantyyppisiä kirjanpitokäytäntöjä:

- Kustannusobjekti
- Syötteen mittaperuste
- Kustannusvirran oletus
- Kustannustaso

> [!NOTE]
> Vaikka olet ottanut yleisen varastokirjanpidon käyttöön, voit silti tehdä varastokirjanpidon Microsoft Dynamics 365 Supply Chain Management -ohjelmassa tavalliseen tapaan.

Yleinen varastokirjanpito on apuohjelma. Jos haluat käyttää sen toimintoja, sinun on asennettava se Microsoft Dynamics Lifecycle Servicesistä (LCS). Voit valita, että se arvioidaan testiympäristössä, ennen kuin otat sen käyttöön tuotantoympäristöissä.

Yleinen varastolaskenta ei tällä hetkellä tue kaikkia Supply Chain Managementiin integroituja kustannustenhallintaominaisuuksia. Tämän vuoksi on tärkeää arvioida, vastaako tällä hetkellä käytössä oleva toimintojoukko tarpeitasi.

## <a name="how-to-get-the-global-inventory-accounting-add-in"></a><a name="sign-up"></a>Yleisen varastolaskennan apuohjelman saaminen

> [!IMPORTANT]
> Jotta voit käyttää yleistä varastokirjanpitoa, sinulla on oltava LCS-yhteensopiva korkean käytettävyyden ympäristö (ei OneBox-ympäristö). Lisäksi käytössä tulee olla Supply Chain Managementin versio 10.0.19 tai sitä myöhempi.

### <a name="supply-chain-management-version-10019-to-10026"></a>Supply Chain Management -versio 10.0.19 – 10.0.26

Asenna yleinen varastokirjanpito Supply Chain Management -versiolle 10.0.19 – 10.0.26 [asentamalla ensin lisäosa](#install). Lähetä sitten LCS-ympäristötunnus ja yrityksen nimi sähköpostitse [yleiselle varastokirjanpitotiimille](mailto:GlobalInvAccount@microsoft.com). Tiimi lähettää sinulle seurantasähköpostiviestin, joka sisältää yleisen varastokirjanpidon huollon päätepisteet.

### <a name="supply-chain-management-version-10027-and-later"></a>Supply Chain Managementin versio 10.0.27 ja uudempi

Asenna yleinen varastokirjanpito Supply Chain Management -versiolle 10.0.27 tai uudemmalle [asentamalla lisäosa](#install). Näissä Supply Chain Management -versioissa yleisen varastonlaskennan palvelun päätepisteet määritetään automaattisesti, joten niitä ei tarvitse etsiä manuaalisesti. Jos apuohjelman määrittämisessä ilmenee ongelmia, ota yhteyttä [yleiseen varastokirjanpitotiimiin](mailto:GlobalInvAccount@microsoft.com).

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

## <a name="install-the-add-in"></a><a name="install"></a>Lisäosan asentaminen

Asenna lisäosa noudattamalla seuraavia ohjeita, jotta voit käyttää yleistä varastokirjanpitoa.

1. Kirjaudu sisään [LCS:ään](https://lcs.dynamics.com/Logon/Index).
1. Avaa LCS-ympäristö, johon haluat lisätä palvelun.
1. Valitse **Kaikki tiedot**.
1. Siirry **Power Platform -integrointiin** ja valitse **Asetukset**.
1. Valitse valintaruutu **Power platform -ympäristön asetus** -valintaikkunassa ja valitse sitten **Asetukset**. Asetusten määritys kestää yleensä 60 - 90 minuuttia.
1. Kun Microsoft Power Platformin ympäristön asetukset on määritetty, kirjaudu sisään [Power Platform -hallintakeskukseen](https://admin.powerplatform.microsoft.com) ja asenna yleisen varastolaskennan apuohjelma seuraavasti:
   1. Valitse ympäristö, johon haluat asentaa apuohjelman.
   1. Valitse **Dynamics 365 -sovellukset**.
   1. Valitse **Asenna sovellus**.
   1. Valitse **Dynamics 365:n yleinen varastokirjanpito**.
   1. Asenna valitsemalla **Seuraava**.
1. Siirry takaisin LCS-ympäristöön. Valitse **Ympäristöapuohjelmat**-pikavälilehdessä **Asenna uusi apuohjelma**.
1. Valitse **Yleinen varastokirjanpito**.
1. Noudata asennusoppaan ohjeita ja hyväksy käyttöehdot.
1. Valitse **Asenna**.
1. **Ympäristön apuohjelmat** -pikavälilehdessä näkyy, että yleistä varastokirjanpitoa asennetaan. Muutaman minuutin kuluttua tilan pitäisi muuttua tilasta *Asennetaan* tilaan *Asennettu*. (Sivu on ehkä päivitettävä, jotta näet tämän muutoksen.) Tässä vaiheessa yleinen varastokirjanpito on valmis käytettäväksi.

Jos Dataverse-asennuksen oletuskieli ei ole englanti, noudata seuraavia ohjeita:
1. Siirry kohtaan **Lisäasetukset \> Hallinta \> Kielet**.
1. Valitse *englanti* (*LanguageCode=1033*) ja valitse **Ota käyttöön**.

## <a name="set-up-the-integration"></a>Määritä integraatio

Seuraavia ohjeita noudattamalla voit määrittää yleisen varastokirjanpidon ja Supply Chain Managementin integroinnin.

1. Kirjaudu Supply Chain Managementiin.
1. Siirry kohtaan **Järjestelmänhallinta \> Ominaisuuksien hallinta**.
1. Valitse **Tarkista päivitysten saatavuus**.
1. Etsi **Kaikki**-välilehdestä toiminto, jonka nimi on *(Esiversio) Yleinen varastokirjanpito*.
1. Valitse **Ota käyttöön nyt**.
1. Siirry kohtaan **Yleinen varastokirjanpito \> Asetukset \> Yleisen varastokirjanpidon parametrit \> Integrointi-parametrit**.
1. Tee jokin seuraavista toimista käytettävän Supply Chain Management -version mukaan:
    - **Supply Chain Management -versio 10.0.19 – 10.0.26**: Syötä **Tietopalvelun päätepiste**- ja **Yleinen varastokirjanpidon päätepiste** -kenttiin URL-osoitteet, jotka on lähetetty sinulle sähköpostitse yleiseltä varastokirjanpidon tiimiltä (katso myös [Yleisen varastolaskennan apuohjelman saaminen](#sign-up)).
    - **Supply Chain Management -versio 10.0.27 ja sitä uudempi**: Päätepisteitä ei tarvitse määrittää, joten voit ohittaa tämän vaiheen.

Yleinen varastokirjanpito on nyt valmis käytettäväksi.
