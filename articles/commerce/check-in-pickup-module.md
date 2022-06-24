---
title: Noudon sisäänkuittaus -moduuli
description: Tässä artikkelissa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.
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
ms.openlocfilehash: 7002db893da1802063148a9b800ffa92f3e5f065
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885472"
---
# <a name="check-in-for-pickup-module"></a>Noudon sisäänkuittaus -moduuli

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan tietoja noutomoduulin sisäänkuittauksesta ja sen määrittämisestä Microsoft Dynamics 365 Commerce -sovellukseen.

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
