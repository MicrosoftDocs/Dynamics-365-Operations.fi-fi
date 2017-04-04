---
title: Tuo valuutanvaihtokurssit
description: "Oikeudellinen yksikkö on saanut laskuja ulkomaan valuutassa, jos on ulkomaan valuutan muuntaminen paikallisena valuuttana. Tämä tarkoittaa sitä, että tarvitaan ajan tasalla eri valuuttojen vaihtokurssit. Tässä aiheessa on yleiskatsaus tarvittavat asetukset ja käsittelyn tuomisen viittaus valuuttakurssien vaihtokurssin tarjoajat, kuten Euroopan keskuspankin ja Venäjän keskuspankin julkaiseman Internetin välityksellä."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Tuo valuutanvaihtokurssit

Oikeudellinen yksikkö on saanut laskuja ulkomaan valuutassa, jos on ulkomaan valuutan muuntaminen paikallisena valuuttana. Tämä tarkoittaa sitä, että tarvitaan ajan tasalla eri valuuttojen vaihtokurssit. Tässä aiheessa on yleiskatsaus tarvittavat asetukset ja käsittelyn tuomisen viittaus valuuttakurssien vaihtokurssin tarjoajat, kuten Euroopan keskuspankin ja Venäjän keskuspankin julkaiseman Internetin välityksellä.

Seuraavissa osissa on tietoja, joita käytetään ja käsitellään valuuttakurssien tuonti.

## <a name="configure-an-exchange-rate-provider"></a>Valuuttakurssi-palvelun määrittäminen
Ennen kuin tuot vaihtokurssit, tiedot, joita tarvitaan tarjoajien, jotka tarjoavat vaihtokurssien mukaan on määritettävä. Käytössä **Määritä vaihtokurssi** vaihtokurssin toimittajat-sivulta. Jotkin palveluntarjoajat vaihtokurssin sisältyvät esittelytiedot Microsoft Dynamics-365 toimintojen. Seuraavassa taulukossa kuvaillaan tämän sivun ohjausobjekteja.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Vaihtokurssipalvelun nimi.                                                                                                                                                                                     |
| **Avain**   | Palvelun tarvitsemien konfigurointitietojen yksilöivä tunnus. Nämä tiedot lisätään automaattisesti valuuttakurssi kunkin palvelun napsauttamalla Lisää **Lisää** painike. |
| **Value** | Jokaisen avaimen tiedot. Nämä tiedot lisätään vaihtokurssin kunkin palvelun napsauttamalla Lisää **Lisää** painike.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Tuo valuutanvaihtokurssit
Voit tuoda valuuttakurssien vaihtokurssin tarjoajien lähteestä ja määrittää ne **valuutanvaihtokurssit** sivulla. Käyttöä **tuo valuutanvaihtokurssit** tuo vaihtokurssit-sivu. Seuraavassa taulukossa on kuvattu kentät, joita tarvitaan Suorita tuonti onnistui.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Vaihtokurssin tyyppi.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Valuuttakurssi-palvelu.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Tämä parametri hallitsee, tuodaanko kuluvan päivän päivämäärän tai päivämäärävälin. Jos haluat ottaa Käytä päivämääräaluetta, kirjoita tai valitse aloitus- ja lopetuspäivämäärät.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Tämä valintaruutu on valittuna hallitsee automaattisen luomisen valuutta paria, jos ei ole valuutta pareja, jotka on tuotu. Tämä vaihtoehto ei ehkä ole käytettävissä, jotkin palveluntarjoajat.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Tämä valintaruutu on valittuna hallitsee nykyisen vaihtokurssin Valuuttaparin päivitys kun on olemassa jo tietyn päivämäärän vaihtokurssia. Valitse tämä valintaruutu, jos vaihtokurssin päivämäärän mukaan ei tuoda, jos toinen vaihtokurssi on jo olemassa.                                                                                       |
| **Prevent import on national holiday** | Tämä valintaruutu on valittuna hallitsee tuonti vaihtokurssin päivämäärän, joka on yleinen vapaapäivä. Esimerkiksi tämä valintaruutu ja käyttää Euroopan keskuspankin valuuttakurssi palveluna, jos järjestelmä ei päivitä vaihtokurssin pyhäpäivä, jotka liittyvät nykyiseen oikeushenkilöön. Tämä vaihtoehto ei ehkä ole käytettävissä, jotkin palveluntarjoajat. |




