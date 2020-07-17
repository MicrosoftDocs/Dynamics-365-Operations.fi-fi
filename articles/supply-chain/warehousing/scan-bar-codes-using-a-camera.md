---
title: Viivakoodien lukeminen kameran avulla varastosovelluksessa
description: Tässä ohjeaiheessa käsitellään varastosovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: a7a7303004620d2e9cef0642b16d89163911dbb4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/01/2020
ms.locfileid: "3530003"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Viivakoodien lukeminen kameran avulla varastosovelluksessa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään varastosovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten. 

## <a name="prerequisites"></a>Edellytykset
Tämän toiminnon käyttämiseen tarvitaan varastosovelluksen versio 1.2.0.0, ja laitteessa on oltava kamera. Kun avaat sovelluksen päivityksen jälkeen, sovellus pyytää lupaasi käyttää kameraa. Jos laiteessa ei ole kameraa, lupaa ei kysytä etkä voi käyttää kameraa skannerina. 

## <a name="setup"></a>Määritys
Voit valita varastosovelluksen näyttöasetuksissa, käytetäänkö kameraa viivakoodin lukemiseen. Jos otat **kameran käytön skannerina** käyttöön, voit käyttää kameraa jokaisessa syöttömenetelmäksi, jonka ensisijaiseksi syötetilaksi on määritetty **Luetaan**. 

Voit määrittää, voiko syötekentän lukea, valitsemalla **Varastosovelluksen kenttien nimet** -sivulla **Ensisijainen syöttömenetelmä** -asetukseksi **Luetaan**. Kun tämä asetus on valittu, kameraa voidaan käyttää skannaukseen varastosovelluksessa. Lisätietoja sovelluskenttien nimien määrittämisestä varastosovelluksessa on kohdassa [Varastosovelluksen kenttien nimien määrittäminen](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Tuetut viivakoodimuodot
Eniten käytettyjä viivakoodimuotoja tuetaan. Niitä ovat esimerkiksi Koodi 128, Koodi 39, Koodi 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodit. 

## <a name="navigation"></a>Siirtyminen
Kamerasivu käynnistetään jokaisella sivulla, jonka syötekentän ensisijaiseksi syöttömenetelmäksi on valittu Luetaan. Voit liikkua Kamera-sivulla seuraavien asetusten avulla:
- Voit palata Tehtävät ja tiedot -sivulle napsauttamalla Takaisin-painiketta. 
- Kun napsautat kynäkuvaketta Tehtävät ja tiedot -sivulla, voit siirtyä sivulle, jossa voit kirjoittaa tiedot manuaalisesti.
- Voit palata Kamera-sivulle napsauttamalla kamerakuvaketta Tehtävät ja tiedot -sivulla. 

| Tehtävät ja tiedot -sivu | Kamera-sivu | 
| :---------------------: | :--------------------: |
| ![Kameranluvun esimerkkitehtävän tietosivu](./media/camera-scanning-example-task-detail-page50.png)          | ![Kameranluvun esimerkkitehtävän pienempi tietosivu](./media/camera-scanning-example-camera-page50.png)          |

Kun napsautat Kamera-sivulla kamerapainiketta, se näkyy himmeänä viivakoodin tunnistusyrityksen ajan. Jos viivakoodia ei tunnisteta 5 sekunnin kuluessa, prosessi aikakatkaistaan ja kamerapainiketta voi taas käyttää. Voit sitten yrittää lukea viivakoodin uudelleen.

Kun osoitat viivakoodia kameralla, saat parhaan tuloksen, kun viivakoodi on kohdistettu viivojen sisälle. Kun viivakoodi on luettu, tulos käsitellään ja siirryt seuraavaan vaiheeseen. Jos seuraavassa vaiheessa on toinen syötekenttä, jonka ensisijaiseksi syöttömenetelmäksi on valittu Luetaan, kamerasivu käynnistyy uudelleen. Jos seuraava vaihe ei ole luettava kenttä, kamerasivu ei käynnisty.

