---
title: Viivakoodien lukeminen kameran avulla varastonhallinnan mobiilisovelluksessa
description: Tässä ohjeaiheessa käsitellään varastonhallinnan mobiilisovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.
author: Mirzaab
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: cc58d88865fea17e0e27463b25e2ba815ee1a5b1
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/09/2021
ms.locfileid: "7901969"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Viivakoodien lukeminen kameran avulla varastonhallinnan mobiilisovelluksessa

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käsitellään varastonhallinnan mobiilisovelluksen määrittämistä mobiililaitteella tapahtuvaa viivakoodien lukemista varten.

## <a name="setup"></a>Luo perustiedot

Voit valita varastonhallinnan mobiilisovelluksen näyttöasetuksissa, käytetäänkö kameraa viivakoodin lukemiseen. Jos otat **kameran käytön skannerina** käyttöön, voit käyttää kameraa jokaisessa syöttömenetelmäksi, jonka ensisijaiseksi syötetilaksi on määritetty **Luetaan**.

Voit määrittää, voiko syötekentän lukea, valitsemalla **Varastosovelluksen kenttien nimet** -sivulla **Ensisijainen syöttömenetelmä** -asetukseksi **Luetaan**. Kun tämä asetus on valittu, kameraa voidaan käyttää skannaukseen varastonhallinnan mobiilisovelluksessa. Lisätietoja: [Varastonhallinnan mobiilisovelluksen kenttien konfigurointi](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Tuetut viivakoodimuodot

Eniten käytettyjä viivakoodimuotoja tuetaan. Niitä ovat esimerkiksi Koodi 128, Koodi 39, Koodi 93, EAN-8, EAN-13, UPC-E, UPC-A ja QR-koodit.

## <a name="navigation"></a>Siirtyminen

Kamerasivu käynnistetään jokaisella sivulla, jonka syötekentän **ensisijaiseksi syöttömenetelmäksi** on valittu *Skannaus*. Voit liikkua Kamera-sivulla seuraavien asetusten avulla:

- Voit palata **Tehtävät ja tiedot** -sivulle napsauttamalla Takaisin-painiketta.
- Kun valitset kynäkuvakkeen **Tehtävät ja tiedot** -sivulla, voit siirtyä sivulle, jossa voit kirjoittaa tiedot manuaalisesti.
- Voit palata kamerasivulle valitsemalla kamerakuvakkeen **Tehtävät ja tiedot** -sivulla.

Kun valitset Kamera-sivulla kamerapainikkeen, se näkyy himmeänä viivakoodin tunnistusyrityksen ajan. Jos viivakoodia ei tunnisteta 5 sekunnin kuluessa, prosessi aikakatkaistaan ja kamerapainiketta voi taas käyttää. Voit sitten yrittää lukea viivakoodin uudelleen.

Kun osoitat viivakoodia kameralla, saat parhaan tuloksen, kun viivakoodi on kohdistettu viivojen sisälle. Kun viivakoodi on luettu, tulos käsitellään ja siirryt seuraavaan vaiheeseen. Jos seuraavassa vaiheessa on toinen syötekenttä, jonka ensisijaiseksi syöttömenetelmäksi on valittu Luetaan, kamerasivu käynnistyy uudelleen. Jos seuraava vaihe ei ole luettava kenttä, kamerasivu ei käynnisty.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]