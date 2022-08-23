---
title: Verkkotehtävätapahtumien keräämisestä kieltäytyminen
description: Tässä artikkelissa käsitellään tapaa, jolla sivustossa vierailijat voivat kieltäytyä verkkotoiminnan tapahtumien keräämisestä Microsoft Dynamics 365 Commercessa.
author: bebeale
ms.date: 05/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.search.industry: Retail, eCommerce
ms.search.form: ''
ms.openlocfilehash: 81343f5033366484140f73fcc313ecd9f35e7d47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286722"
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
