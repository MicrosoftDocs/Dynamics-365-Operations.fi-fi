---
title: Hyllytyksen päivitysseuranta
description: Tässä aiheessa kuvataan, miten kausittaisen tehtävän päivityksen seuranta määritetään ja suoritetaan.
author: sherry-zheng
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d8e2a42d8e12a5a9cf18e876b6f9e45ecb877881
ms.sourcegitcommit: ecd4c148287892dcd45656f273401315adb2805e
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 09/18/2021
ms.locfileid: "7500020"
---
# <a name="update-tracking-for-put-away"></a>Hyllytyksen päivitysseuranta

[!include [banner](../includes/banner.md)]

*Kausittaisen hyllytyksen päivityksen seuranta* on suunniteltu suoritettavaksi yöllä toistuvana eränä. Se tunnistaa, mitkä matkat ovat vastaanottaneet kaikki varastotapahtumat ja millä matkoilla ei ole arvoa todelliselle lopetuspäivälle. Sen jälkeen todellinen päättymispäivä määritetään tarvittaessa nykyiseksi päivämääräksi.

*Konttitoiminnot* luodaan kullekin matkan *osalle* kullekin *kuljetuskontille*. Nämä arvot määritetään sen mallin avulla, joka valitaan, kun matka luodaan. Jokaisen konttitoiminnottietueen arvot voidaan määrittää **aloituspäivä**-, **arvioitu päättymispäivä**- ja **todellinen päättymispäivä** -kentille. Nämä kentät voidaan päivittää, kun vahvistus vastaanotetaan, että matkan osa on alkanut tai on valmistunut.

Tavallisesti vahvistettuihin päivämääriin liittyvät tiedot antaa kolmas osapuoli, kuten rahdinkuljetus, koska nämä toimenpiteet säilytetään Microsoft Dynamics 365 Supply Chain Managementin ulkopuolella. Kolmannen osapuolen tietoja ei kuitenkaan vaadita, jotta voidaan seurata tavaroiden saapumista matkalta varastoon (tavaran poistamisen merkitsemänä). Seuranta voidaan näin ollen määrittää Dynamics 365 Supply Chain Managementin tietojen perusteella.

Määritä ja suorita *päivitysten seuranta kausittaisen poistamisen aikana* seuraavasti:

1. Siirry kohtaan **Aiheutuneet kustannukset \> Kausittaiset tehtävät \> Poispanon seurannan päivitys**.
1. Määritä seuraavat kentät **Poispanon päivityksen seuranta** -valintaikkunassa **Parametrit**-osassa:

    - **Matka** – Valitse yksilöllinen tunnistenimi/-numero matkalle, jonka seurannan haluat päivittää. Valitun arvon on edustettava matkan saapumista varastoon.
    - **Tehtävä** – Valitse tehtävä, joka on tehty valitun matkan osan aikana. Nämä arvot määritetään seurantakeskuksen malliriviä kohti.

1. Voit rajoittaa päivitykseen sisällytettävien tietueiden joukkoa valitsemalla **Suodata**-painikkeen **Sisällytettävät tietueet** -pikavälilehdeltä. Näyttöön tulee vakiokyselyvalintalaatikko, jossa voit määrittää valintaehtoja, lajitteluehtoja ja liitoksia. Kentät toimivat samalla tavalla kuin muissakin kyselyissä Supply Chain Managementissa. Tämän lomakkeen kentät ovat vain luku -kenttiä, ja ne näyttävät kyselyyn liittyviä arvoja.
1. Määritä **Suorita taustalla** -pikavälilehdessä tarvittavat erä- ja aikataulutusvaihtoehdot aivan kuten muissakin Supply Chain Managementin työtyypeissä.
1. Ota asetukset käyttöön ja suorita tai ajoita päivitys valitsemalla **OK**.
