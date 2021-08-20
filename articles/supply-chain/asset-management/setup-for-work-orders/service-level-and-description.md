---
title: Palvelutaso ja kuvaus
description: Tässä ohjeaiheessa kerrotaan palvelutasosta ja kuvauksesta resurssien hallinnassa.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectServiceLevel, EntAssetWorkOrderStandardDescription, EntAssetWorkOrderServiceLevel, EntAssetServiceLevelLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 32e6dd6ba7291e8ea1cb78eeed2d8e2fcec0f6dd3cbd039336be0169730101ba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6758685"
---
# <a name="service-level-and-description"></a>Palvelutaso ja kuvaus

[!include [banner](../../includes/banner.md)]

 

Kun luot työtilauksen, haluat ehkä määrittää sen palvelutasot ja lisätä siihen yleisen kuvauksen. Voit luoda työtilauspalvelutasoja **Työtilauksen palvelutasot** -sivulla ja kuvaukset **Työtilauksen kuvaus** -sivulla.

## <a name="create-a-service-level"></a>Luo palvelutaso

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Palvelutaso**.
2. Valitse **Uusi**.
3. Kirjoita **Palvelutaso**-kenttään palvelutaso (esimerkiksi numero).
4. Anna nimi **Nimi**-kenttään.

    **Työtilaukset**-pikavälilehdessä voit määrittää odotetut alkamis- ja päättymispäivämäärät sekä -ajat. Tämän pikavälilehden kentissä määritetään kausi, jolloin työtilaukset aloitetaan ja päätetään. Niitä käytetään manuaalisesti luoduissa työtilauksissa ja kunnossapitopyyntöjen perusteella luoduissa työtilauksissa. 

5. Kirjoita **Aloituspäivä**-kenttään päivien lukumäärä, joka määrittää työtilauksen aloitusajan ajanjakson. Päivien määrä lasketaan työtilauksen luontipäivästä. Jos esimerkiksi työtilauksen pitäisi alkaa luonnin yhteydessä, kirjoita **0.** Jos työtilauksen pitäisi alkaa viikko luonnin jälkeen, kirjoita **7.**
6. Jos haluat määrittää työtilaukselle aloitusajan aloituspäivämäärän lisäksi, määritä **Aseta aloitusaika** -asetukseksi **Kyllä.** Kirjoita aloitusaika **Aloitusaika**-kenttään. Jos määrität asetukseksi **Ei**, käytetään nykyistä kellonaikaa.
7. Kirjoita **Päättymispäivä**-kenttään päivien lukumäärä, joka määrittää työtilauksen päättymisajan ajanjakson. Päivien määrä lasketaan työtilauksen aloituspäivästä. Jos esimerkiksi työtilauksen pitäisi päättyä viikon kuluttua sen alkamispäivästä, kirjoita **7.**
8. Jos haluat määrittää työtilaukselle päättymisajan päättymispäivämäärän lisäksi, määritä **Aseta päättymisaika** -asetukseksi **Kyllä.** Kirjoita päättymisaika **Päättymisaika**-kenttään. Jos määrität asetukseksi **Ei**, käytetään nykyistä kellonaikaa.
9. Valitse **Tallenna**.

![Työtilausten palvelutasosivu.](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Luo kuvaus

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Kuvaukset**.
2. Valitse **Uusi**.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Tallenna**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]