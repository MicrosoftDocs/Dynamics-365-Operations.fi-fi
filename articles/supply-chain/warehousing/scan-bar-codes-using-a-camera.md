---
title: "Viivakoodien lukeminen kameralla Dynamics 365 for Finance and Operations – Warehousingissa"
description: "Tässä ohjeaiheessa käsitellään Dynamics 365 for Finance and Operations – Warehousingin määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: fi-fi
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Viivakoodien lukeminen kameralla Dynamics 365 for Finance and Operations – Warehousingissa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Finance and Operations – Warehousingin määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten. 

## <a name="prerequisites"></a>Edellytykset
Tämän toiminnon käyttämiseen tarvitaan Warehousing 1.2.0.0, ja laitteessa on oltava kamera. Kun avaat sovelluksen päivityksen jälkeen, sinua pyydetään sallimaan kameran käyttö Dynamics 365 for Finance and Operations – Warehousing -sovelluksessa. Jos laiteessa ei ole kameraa, lupaa ei kysytä etkä voi käyttää kameraa skannerina. 

## <a name="setup"></a>Määritys
Voit valita Warehousing-sovelluksen näyttöasetuksissa, käytetäänkö kameraa viivakoodin lukemiseen. Jos otat **kameran käytön skannerina** käyttöön, voit käyttää kameraa jokaisessa syöttömenetelmäksi, jonka ensisijaiseksi syötetilaksi on määritetty **Luetaan**. 

Voit määrittää, voiko syötekentän lukea, valitsemalla Dynamics 365 for Finance and Operationsin **Varastosovelluksen kenttänimet** -sivulla **Ensisijainen syöttömenetelmä** -asetukseksi **Luetaan**. Kun tämä asetus on valittu, kameraa voidaan käyttää skannaukseen Warehousing-sovelluksessa. Lisätietoja sovelluskenttien nimien määrittämisestä Warehousing-sovelluksessa on kohdassa [Warehousing-sovelluksen kenttien nimien määrittäminen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Tuetut viivakoodimuodot
Eniten käytettyjä viivakoodimuotoja tuetaan. Niitä ovat esimerkiksi Koodi 128, Koodi 39, Koodi 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodit. 

## <a name="navigation"></a>Siirtyminen
Kamerasivu käynnistetään jokaisella sivulla, jonka syötekentän ensisijaiseksi syöttömenetelmäksi on valittu Luetaan. Voit liikkua Kamera-sivulla seuraavien asetusten avulla:
- Voit palata Tehtävät ja tiedot -sivulle napsauttamalla Takaisin-painiketta. 
- Kun napsautat kynäkuvaketta Tehtävät ja tiedot -sivulla, voit siirtyä sivulle, jossa voit kirjoittaa tiedot manuaalisesti.
- Voit palata Kamera-sivulle napsauttamalla kamerakuvaketta Tehtävät ja tiedot -sivulla. 

| Tehtävät ja tiedot -sivu | Kamera-sivu | 
| :---------------------: | :--------------------: |
| ![kamera-luetaan-esimerkki-tehtävä-tiedot-sivu](./media/camera-scanning-example-task-detail-page50.png)          | ![kamera-luetaan-esimerkki-kamera-sivu-pieni](./media/camera-scanning-example-camera-page50.png)          |

Kun napsautat Kamera-sivulla kamerapainiketta, se näkyy himmeänä viivakoodin tunnistusyrityksen ajan. Jos viivakoodia ei tunnisteta 5 sekunnin kuluessa, prosessi aikakatkaistaan ja kamerapainiketta voi taas käyttää. Voit sitten yrittää lukea viivakoodin uudelleen.

Kun osoitat viivakoodia kameralla, saat parhaan tuloksen, kun viivakoodi on kohdistettu viivojen sisälle. Kun viivakoodi on luettu, tulos käsitellään ja siirryt seuraavaan vaiheeseen. Jos seuraavassa vaiheessa on toinen syötekenttä, jonka ensisijaiseksi syöttömenetelmäksi on valittu Luetaan, kamerasivu käynnistyy uudelleen. Jos seuraava vaihe ei ole luettava kenttä, kamerasivu ei käynnisty.


