---
title: Tuo valuutanvaihtokurssit
description: "Jos oikeudellinen yksikkö on saanut laskuja ulkomaan valuutassa, on tarpeen muuntaa ulkomaan valuutta paikalliseksi valuutaksi. Tämä tarkoittaa sitä, että tarvitaan ajan tasalla olevat eri valuuttojen vaihtokurssit. Tässä aiheessa on yleiskatsaus tarvittavista asetuksista ja käsittelystä ulkomaiden valuuttakurssien viitekurssien tuomisesta, jotka on julkaistu internetissä vaihtokurssien tarjoajien toimesta, kuten Euroopan keskuspankin ja Venäjän keskuspankin."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: df07066371cb7d9c69976c9714b6d2fe456a0308
ms.contentlocale: fi-fi
ms.lasthandoff: 03/26/2018

---

# <a name="import-currency-exchange-rates"></a>Tuo valuutanvaihtokurssit

[!INCLUDE [banner](../includes/banner.md)]

Jos oikeudellinen yksikkö on saanut laskuja ulkomaan valuutassa, on tarpeen muuntaa ulkomaan valuutta paikalliseksi valuutaksi. Tämä tarkoittaa sitä, että tarvitaan ajan tasalla olevat eri valuuttojen vaihtokurssit. Tässä aiheessa on yleiskatsaus tarvittavista asetuksista ja käsittelystä ulkomaiden valuuttakurssien viitekurssien tuomisesta, jotka on julkaistu internetissä vaihtokurssien tarjoajien toimesta, kuten Euroopan keskuspankin ja Venäjän keskuspankin.

Seuraavissa osissa kuvataan ulkomaiden valuuttakurssien tuomisen määrittämisessä ja käsittelyssä käytettävää tiedonkulkua.

## <a name="configure-an-exchange-rate-provider"></a>Konfiguroi vaihtokurssipalvelu
Ennen kuin tuot vaihtokurssit, tiedot, joita tarvitaan tarjoajille, jotka tarjoavat vaihtokurssit, on määritettävä. Valitse vaihtokurssin toimittajat **Konfiguroi vaihtokurssipalvelut** -sivulla. Jotkin vaihtokurssin palveluntarjoajat sisältyvät Microsoft Dynamics 365 for Finance and Operationsin esittelytietoihin. Seuraavassa taulukossa kuvaillaan tämän sivun ohjausobjektit.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kenttä** | **Kuvaus**                                                                                                                                                                                                             |
| **Nimi**  | Vaihtokurssipalvelun nimi.                                                                                                                                                                                     |
| **Avain**   | Palvelun tarvitsemien konfigurointitietojen yksilöivä tunnus. Nämä tiedot lisätään automaattisesti jokaiseen vaihtokurssipalveluun, jonka lisäät **Lisää**-painiketta napsauttamalla. |
| **Arvo** | Jokaisen avaimen tiedot. Nämä tiedot lisätään jokaiseen vaihtokurssipalveluun, jonka lisäät **Lisää**-painiketta napsauttamalla.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Tuo valuutanvaihtokurssit
Voit tuoda valuuttakurssit vaihtokurssin tarjoajien lähteestä ja määrittää ne **Valuutan vaihtokurssit** -sivulla. Käytä **Tuo valuutanvaihtokurssit** -sivua tuodaksesi vaihtokurssit. Seuraavassa taulukossa on kuvattu kentät, joita tarvitaan tuontiprosessin onnistuneeseen suorittamiseen.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kenttä**                              | **Kuvaus**                                                                                                                                                                                                                                                                                                                                                             |
| **Vaihtokurssin tyyppi**                 | Vaihtokurssin tyyppi.                                                                                                                                                                                                                                                                                                                                                      |
| **Vaihtokurssipalvelu**             | Vaihtokurssipalvelu.                                                                                                                                                                                                                                                                                                                                                  |
| **Tuo päivämäärätyypillä**                       | Tämä parametri hallitsee, tuodaanko kuluvan päivän mukaan vai päivämääräväliltä. Jos haluat käyttää päivämääräväliä, valitse tai kirjoita alku- ja loppupäivämäärä.                                                                                                                                                                                                                |
| **Luo tarvittavat valuuttaparit**    | Tämä valintaruutu hallitsee valuuttaparien automaattista luomista, jos ei ole tuotavia valuuttapareja ei ole. Tämä vaihtoehto ei ehkä ole käytettävissä, joillakin palveluntarjoajilla.                                                                                                                                                                                               |
| **Korvaa aiemmat vaihtokurssit**   | Tämä valintaruutu hallitsee valuuttaparin nykyisen vaihtokurssin päivitystä, kun on olemassa jo tietyn päivämäärän vaihtokurssi. Jos et valitse tätä valintaruutua, tiettyjen päivämäärien vaihtokurssia ei tuoda, jos toinen vaihtokurssi on jo olemassa.                                                                                       |
| **Estä tuonti kansallisina vapaapäivinä** | Tämä valintaruutu hallitsee tuontia vaihtokurssille päivämääränä, joka on yleinen vapaapäivä. Jos esimerkiksi valitset tämän valintaruudun ja käytät Euroopan keskuspankkia valuuttakurssipalveluna, järjestelmä ei päivitä vaihtokurssia pyhäpäivänä, joka liittyy nykyiseen oikeushenkilöön. Tämä vaihtoehto ei ehkä ole käytettävissä, joillakin palveluntarjoajilla. |






