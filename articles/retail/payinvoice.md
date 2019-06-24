---
title: Laskun maksutapojen määrittäminen
description: Tässä aiheessa kuvataan, miten voit konfiguroida Dynamics 365 for Retailin tukemaan erilaisia laskun maksamiseen liittyviä tilanteita.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b7132dc9b3c78fa04fcfc38ea72b5678ad08deb2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564967"
---
# <a name="set-up-pay-invoice-scenarios"></a>Laskun maksutapojen määrittäminen

[!include [banner](includes/banner.md)]

Dynamics 365 for Retailin Maksa lasku -toiminnallisuutta on laajennettu tukemaan seuraavia tilanteita:

- Useiden myyntitilauslaskujen maksaminen yhdessä myyntipistetapahtumassa.
- Erilaisten asiakaslaskutyyppien, esimerkiksi vapaatekstilaskujen, projektiin perustuvien laskujen ja hyvityslaskujen, maksaminen.

Näiden ominaisuuksien käyttöönottamiseksi myymälöiden toimintoprofiili on määritettävä alla kuvatulla tavalla.

1. Siirry kohtaan **Vähittäismyynti \> Kanavan asetukset \> POS-asetukset \> POS-profiilit \> Toimintoprofiilit** ja valitse profiili, joka on linkitetty myymälöihin, joita haluat muutoksen koskevan.
2. Määritä **Toiminnot**-välilehdessä seuraavat parametrit tarpeen mukaan.

    - **Myyntitilauslasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman myyntitilaukseen perustuvan laskun yhdessä myyntipistetapahtumassa.
    - **Vapaatekstilasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman vapaatekstilaskun yhdessä myyntipistetapahtumassa.
    - **Projektilasku** – Valitse **Kyllä**, jotta käyttäjät voivat maksaa yhden tai useamman projektiin perustuvan laskun yhdessä myyntipistetapahtumassa.
    - **Myyntitilauksen hyvityslasku** – Valitse **Kyllä**, jotta käyttäjät voivat selvittää useita myyntitilaukseen perustuvia hyvityslaskuja avoimet laskut huomioiden tai käsitellä avoimen hyvityslaskun hyvityksen asiakkaalle.

> [!NOTE]
> Osittaisten summien maksua tai selvitystä ei vielä tueta.
