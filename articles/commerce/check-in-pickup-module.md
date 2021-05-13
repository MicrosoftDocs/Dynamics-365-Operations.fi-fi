---
title: Noutomoduulin sisäänkuittaus
description: Tässä aiheessa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
author: bicyclingfool
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: e7bae4ae7c2f3367132b03accb31c01c5f3b673e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937580"
---
# <a name="check-in-for-pickup-module"></a>Noutomoduulin sisäänkuittaus

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Tässä aiheessa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

Noutomoduulin sisäänkuittaus toimii vahvistussivuna asiakkaille, jotka käyttävät Dynamics 365 Commercen asiakkaan sisäänkuittaustoimintoja ilmoittaakseen myymälälle saapumisestaan. Noutomoduulin sisäänkuittauksessa voi myös konfiguroida lomakkeen, joka kerää asiakkailta lisätietoja tilausten toimitusta varten. Näitä tietoja ovat asiakkaan pysäköintipaikan numero sekä ajoneuvon merkki ja malli. 

## <a name="module-properties"></a>Moduulin ominaisuudet

| Ominaisuuden nimi | Arvot | kuvaus |
|---------------|--------|-------------|
| Vahvistusteksti | Tekstimerkkijono | Sisäänkuittauksen vahvistussivulla näkyvän otsikon sisältö. |
| Näytä QR-koodi | **Tosi** vai **Epätosi** | Kun ominaisuuden arvoksi määritetään **Tosi**, sisäänkuittauksen vahvistussivulla näkyy tilauksen vahvistustunnusta vastaava QR-koodi. |
| Lisätieto-otsikko | Tekstimerkkijono | Sisältö otsikolle, joka tulee näkyviin, kun lisätietokentät on konfiguroitu. |
| Lisätietoavaimet | Resurssitunnus/resurssiarvo-pari | Kukin avain luo lomakekentän ja siihen liittyvän otsikon, jota käytetään lisätietojen keräämiseen asiakkailta. |
| Lisätietoavaimet \> Resurssitunnus | Tekstimerkkijono | Kukin tietoavain luo lomakekentän ja siihen liittyvän otsikon, jota käytetään lisätietojen keräämiseen asiakkailta. Tämä ominaisuus määrittää lisätietoavaimen. Myyntipisteessä luodussa tehtävässä tämän ominaisuuden arvo näkyy ohjeet-kentässä otsikkona. |
| Lisätietoavaimet \> Resurssiarvo | Tekstimerkkijono | Myyntipisteen tehtävän tekstikentän otsikko. |
| Lisätietoavaimet \> Vaaditaan | **Tosi** vai **Epätosi** | Tämä ominaisuus määrittää, onko asiakkaiden täytettävä lomakekenttä ennen jatkamista. Kun ominaisuuden arvoksi määritetään **Tosi**, lomakkeen otsikon viereen muodostetaan tähti ja tyhjäarvon tarkistuksen tekeminen estää asiakkaita jatkamasta, jos arvoa ei ole annettu. |

## <a name="add-the-check-in-for-pickup-module-to-a-page"></a>Noutomoduulin sisäänkuittauksen lisääminen sivulle

Noutomoduulin sisäänkuittaus tulee lisätä uudelle sivulle, joka luodaan sisäänkuittauksen vahvistusta varten. Tätä sivua käytetään sisäänkuittauksen vahvistuskokemuksena asiakkaille, jotka valitsevat sähköpostinsa **Olen paikalla** -linkin tai -painikkeen. 

## <a name="configure-the-additional-information-form"></a>Lisätietolomakkeen määrittäminen

Jos lisätietoavaimia ei ole määritetty, moduulissa näkyy asiakkaille oletusarvon mukaan sisäänkuittauksen vahvistussivu. Kun sisäänkuittauksen vahvistus on näkyvissä, myyntipistepäätteessä luodaan tehtävä myymälälle, josta tilaus kerätään.

Kun vähintään yksi lisätietoavain on konfiguroitu, asiakkaita pyydetään syöttämään tiedot. Kun he valitsevat **Lähetä**, he näkevät sisäänkuittauksen vahvistuksen ja tehtävä luodaan myyntipisteessä. 

## <a name="additional-resources"></a>Lisäresurssit

[Asiakkaan sisäänkuittausilmoitusten ottaminen käyttöön myyntipisteessä](enable-customer-check-in.md)
