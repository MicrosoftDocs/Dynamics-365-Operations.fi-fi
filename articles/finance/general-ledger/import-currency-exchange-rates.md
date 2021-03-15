---
title: Vaihtokurssien tuonti
description: Tässä ohjeaiheessa on tietoja valuuttakurssitoimittajien julkaisemien ulkomaanvaluutan viitekorkojen tuonnin vaatimuksista.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: a5dbe0d822f7bdb1a62a99c43ef9f7170c889676
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988874"
---
# <a name="import-currency-exchange-rates"></a>Vaihtokurssien tuonti

[!include [banner](../includes/banner.md)]

Jos oikeudellinen yksikkö on saanut laskuja ulkomaan valuutassa, tulee muuntaa ulkomaan valuutta paikalliseksi valuutaksi. Tämä tarkoittaa sitä, että tarvitaan ajan tasalla olevat eri valuuttojen vaihtokurssit. Tässä aiheessa on yleiskatsaus tarvittavista asetuksista ja käsittelystä ulkomaiden valuuttakurssien viitekurssien tuomisesta, jotka on julkaistu vaihtokurssien tarjoajien toimesta, kuten Euroopan keskuspankin ja Venäjän keskuspankin.

Seuraavissa osissa kuvataan ulkomaiden valuuttakurssien tuomisen määrittämisessä ja käsittelyssä käytettävää tiedonkulkua.

## <a name="configure-an-exchange-rate-provider"></a>Konfiguroi vaihtokurssipalvelu
Ennen kuin tuot vaihtokurssit, tiedot, joita tarvitaan tarjoajille, jotka tarjoavat vaihtokurssit, on määritettävä. Valitse vaihtokurssin toimittajat **Konfiguroi vaihtokurssipalvelut** -sivulla. Jotkin vaihtokurssin palveluntarjoajat sisältyvät Dynamics 365 Financein esittelytietoihin. Seuraavassa taulukossa kuvaillaan tämän sivun ohjausobjektit.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kenttä** | **Kuvaus**                                                                                                                                                                                                             |
| **Nimi**  | Vaihtokurssipalvelun nimi.                                                                                                                                                                                     |
| **Avain**   | Palvelun tarvitsemien konfigurointitietojen yksilöivä tunnus. Nämä tiedot lisätään automaattisesti jokaiseen vaihtokurssipalveluun, jonka lisäät. |
| **Value** | Jokaisen avaimen tiedot. Nämä tiedot lisätään jokaiseen vaihtokurssipalveluun, jonka lisäät.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Vaihtokurssien tuonti
Voit tuoda valuuttakurssit vaihtokurssin tarjoajien lähteestä ja lisätä ne **Valuutan vaihtokurssit** -sivulle. Käytä **Tuo valuutanvaihtokurssit** -sivua tuodaksesi vaihtokurssit. Seuraavassa taulukossa on kuvaus kentistä, joita tarvitaan tuontiprosessin onnistuneeseen suorittamiseen.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Kenttä**                              | **Kuvaus**                                                                                                                                                                                                                                                                                                                                                             |
| **Vaihtokurssin tyyppi**                 | Vaihtokurssin tyyppi.                                                                                                                                                                                                                                                                                                                                                      |
| **Vaihtokurssipalvelu**             | Vaihtokurssipalvelu.                                                                                                                                                                                                                                                                                                                                                  |
| **Tuo päivämäärätyypillä**                       | Tämä parametri hallitsee, tuodaanko kuluvan päivän mukaan vai tietyltä päivämääräväliltä. Jos haluat käyttää päivämääräväliä, valitse tai kirjoita alku- ja loppupäivämäärä.                                                                                                                                                                                                                |
| **Luo tarvittavat valuuttaparit**    | Tämä valintaruutu hallitsee valuuttaparien automaattista luomista, jos ei ole tuotavia valuuttapareja ei ole. Tämä vaihtoehto ei ehkä ole käytettävissä, joillakin palveluntarjoajilla.                                                                                                                                                                                               |
| **Korvaa aiemmat vaihtokurssit**   | Tämä valintaruutu hallitsee valuuttaparin nykyisen vaihtokurssin päivitystä, kun on olemassa jo tietyn päivämäärän vaihtokurssi. Jos et valitse tätä valintaruutua, tiettyjen päivämäärien vaihtokurssia ei tuoda, jos toinen vaihtokurssi on jo olemassa.                                                                                       |
| **Estä tuonti kansallisina vapaapäivinä** | Tämä valintaruutu hallitsee yleisten vapaapäivien valuuttakurssien tuontia. Jos esimerkiksi valitset tämän valintaruudun ja käytät Euroopan keskuspankkia valuuttakurssipalveluna, järjestelmä ei päivitä vaihtokurssia pyhäpäivänä, joka liittyy nykyiseen oikeushenkilöön. Tämä vaihtoehto ei ehkä ole käytettävissä, joillakin palveluntarjoajilla. |
| **Edellisen päivän kurssi** | Tämä valintaruutu on käytettävissä, jos otat **EKP-tuonnin käyttöön nykyisellä tai edellisellä päivämäärä** -toiminnolla **Toimintojen hallinta** -sivulla. Tämä valintaruutu on käytettävissä vain toimittajalle, *Euroopan keskuspankille*. Valitse tämä valintaruutu, jos haluat tuoda valuutan vaihtokurssin, jonka Euroopan keskuspankki on julkaissut edellisenä työpäivänä noin kello 16.00 CET. Oletuksena Hyväksytty-valintaruutu on valittu. Poistamalla tämän valintaruudun valinnan voit tuoda saman työpäivän aikana julkaistun valuutanvaihtokurssin.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]