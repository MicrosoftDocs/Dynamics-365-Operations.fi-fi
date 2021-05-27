---
title: Dynamics 365 -globalisointipalvelut
description: Tässä aiheessa on yleiskuvaus Microsoft Dynamics 365 -globalisointipalveluista.
author: JaneA07
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 2ef942f7f6dac2c321a51800ade0bf25f2162304
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018804"
---
# <a name="dynamics-365-globalization-services"></a>Dynamics 365 -globalisointipalvelut

[!include [banner](../includes/banner.md)]

Seuraavat globalisointipalvelut voidaan konfiguroida laajentamaan joidenkin Microsoft Dynamics 365 -verkkopalvelun ominaisuuksia:

- **Regulatory Configuration Service (RCS)** tukee erilaisten sähköisten tiedostojen ja raporttien konfiguroinnissa. RCS tarjoaa sähköisen raportoinnin (ER) parannetun version, jossa konfigurointitietovarasto on erillinen palvelu. Lisätietoja on kohdassa [Regulatory Configuration Service](rcs-overview.md).
- **Sähköinen laskutus** kokoaa yhteen muunnosten, digitaalisten allekirjoitusten ja konfiguroitavia integrointien muotoja, joita voidaan konfiguroida ulkoisten Internet-palveluiden kanssa, mukaan lukien sertifikaattien ja vastausten käsittely. Lisätietoja kohdassa [Sähköinen laskutus](e-invoicing-service-overview.md).
- **Verojen laskenta** mahdollistaa joustavan suorituksen tukemalla useita verotunnuksia, verokoodin määrittämisen, veron laskentasuunnittelijan ja ajoaikaohjelman, jotka noudattavat monimutkaisia verosäädöksiä maailmanlaajuisesti. Lisätietoja on kohdassa [Verolaskenta](global-tax-calcuation-service-overview.md).

Nämä globalisointipalvelut tarjoavat ruudukkointegraation seuraavien Dynamics 365 -verkkopalveluiden kanssa.

| Verkkopalvelut | Sääntöjen konfigurointipalvelu | Sähköinen laskutus | Verolaskenta (esiversio) |
|----------------|-----|----------------------|---------------------------|
| Dynamics 365 Finance | Kyllä | Kyllä | Kyllä | 
| Dynamics 365 Supply Chain Management | Kyllä | Kyllä | Kyllä | 
| Dynamics 365 Project Operations | Kyllä | Kyllä | Ei käytettävissä | 
| Dynamics 365 Commerce | Kyllä | Ei käytettävissä | Ei käytettävissä | 

> [!NOTE]
> Azuren maantieteellisten sijaintien (geos) saatavuuden erojen vuoksi RCS:lle tämän palvelun määritys saattaa aiheuttaa asiakastietojen siirtämisen sovellettavaan Dynamics 365 -verkkopalveluun valitun maantieteellisen alueen ulkopuolelle. Lisätietoja on kohdassa [Dynamics 365 ja Power Platform: Saatavuus, tietojen sijainti, kieli ja localization](https://aka.ms/rcs/D365Productavailabilityguide).