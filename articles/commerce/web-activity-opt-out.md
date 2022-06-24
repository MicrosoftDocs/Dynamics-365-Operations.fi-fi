---
title: Verkkotehtävätapahtumien keräämisestä kieltäytyminen
description: Tässä artikkelissa käsitellään tapaa, jolla sivustossa vierailijat voivat kieltäytyä verkkotoiminnan tapahtumien keräämisestä Microsoft Dynamics 365 Commercessa.
author: aamiral
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 78d3f795820eb36d1a81fb28875456e7471f8971
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878396"
---
# <a name="opt-out-of-web-activity-event-collection"></a>Verkkotehtävätapahtumien keräämisestä kieltäytyminen
[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään, miten asiakkaat voivat kieltäytyä verkkotoiminnan tapahtumien keräämisestä Microsoft Dynamics 365 Commercessa.

Dynamics 365 Commerce antaa sivuston järjestelmänvalvojille mahdollisuuden analysoida käyttäjien verkkotoimintaa omissa sähköisen kaupankäynnin sivustoissa. Tällä tavoin he saavat paremman käsityksen tavasta, jolla sivustoja käytetään. Lisäksi he voivat optimoida sivustoja niin, että niiden käyttökokemus paranee ja liiketoimintatavoitteet saavutetaan.


## <a name="ways-for-administrators-to-implement-an-opt-out-experience"></a>Tapoja, joilla järjestelmänvalvojat voivat toteuttaa kieltäytymiskokemuksen

Järjestelmänvalvojat voivat toteuttaa kieltäytymiskokemuksen kolmella tavalla.

### <a name="opt-out-on-behalf-of-users"></a>Kieltäytyminen käyttäjien puolesta

Järjestelmänvalvojat voivat kieltäytyä käyttäjien puolesta Commercen pääkonttoriosan (HQ) tilien hallinnassa.

1. Asiakas voidaan hakea ja valita HQ-asiakasohjelman **Kaikki asiakkaat** -sivulla.
1. **Älä seuraa verkkotoimintaa** -asetukseksi määritetään **Kyllä** asiakastietosivun **Vähittäismyynti**-pikavälilehden **Tietosuoja**-osassa.

    ![Tietosuoja-asetukset.](media/Disablepersonalizationpart2.png)

1. Valitse **Tallenna** ja sulje sitten sivu.

### <a name="module-based-opt-out-experience"></a>Moduulipohjainen opt-out-kokemus

Järjestelmänvalvojat voivat antaa todennettujen käyttäjien kieltäytyä itse verkkotoiminnan tapahtumien keräämisestä. Voit antaa tämän opt-out-käyttökokemuksen lisäämällä käyttäjän opt-out-moduulin asiakastilin profiilisivuille.

### <a name="custom-extensions"></a>Mukautetut laajennukset

Järjestelmänvalvojat voivat luoda omia laajennuksia, joilla hallitaan käyttäjien käyttöoikeustietoja. Lisätietoja on kohdassa [Soita Retail-palvelimen ohjelmointirajapinnalle](e-commerce-extensibility/call-retail-server-apis.md) ja [Online-kanavan laajennettavuus](e-commerce-extensibility/overview.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
