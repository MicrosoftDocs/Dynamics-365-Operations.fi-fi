---
title: Palvelutaso ja kuvaus
description: Tässä ohjeaiheessa kerrotaan palvelutasosta ja kuvauksesta resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5e645c25208f55b1032bc7f7c181c72db7a2f265
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874644"
---
# <a name="service-level-and-description"></a>Palvelutaso ja kuvaus

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

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

![Kuva 1](media/19-setup-for-work-orders.png)

## <a name="create-a-description"></a>Luo kuvaus

1. Valitse **Resurssien hallinta** \> **Asetukset** \> **Työtilaukset** \> **Kuvaukset**.
2. Valitse **Uusi**.
3. Syötä **Kuvaus**-kenttään kuvaus.
4. Valitse **Tallenna**.