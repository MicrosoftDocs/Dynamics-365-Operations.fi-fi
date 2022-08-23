---
title: Vähittäismyynnin hintaraportit
description: Tässä artikkelissa on hintaraporttitoiminnon yleiskatsaus. Tämän toiminnon avulla voidaan tarkastella lajiteltujen tuotteiden tulevia hintamuutoksia.
author: ShalabhjainMSFT
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.region: global
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.industry: Retail
ms.search.form: ''
ms.openlocfilehash: 09350d15660978126d36199a3b4e93f6be5fe157
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269024"
---
# <a name="retail-price-reports"></a>Vähittäismyyntihintaraportit

[!include [banner](includes/banner.md)]


Jotta hinnat olisivat kilpailukykyisiä, vähittäismyyjät muuttavat usein tuotteiden hintoja. Myymäläpäälliköt haluavat, että pääsevät helposti käsiksi äskettäisiin tau tuleviin hintamuutoksiin, jotta he voivat suunnitella tarvittavat resurssit myymälän hyllyissä näkyvien hintalappujen päivittämiseen. Retailin versiossa 10.0 myymäläpäällikkö voi avata **Hinta**-raportin valitsemalla **Kaikki vähittäismyymälät \> Myymälä \> Hintaraportti** ja tarkastelemalla myymälään liitettyjen tuotteiden päivitettyjä hintoja. 

Hintaraportti voidaan ottaa käyttöön, kun **Ota myymälän hintaraportti käyttöön** -parametrin on oltava käytössä. Tämä parametri sijaitsee **Commercen parametrit \> Alennukset \> Muut**-välilehdessä. Kun **Hintaraportti**-sivu avataan, avautuvassa valintaikkunassa on useita määrityksiä. Käytettävissä olevat määritykset on lueteltu seuraavaksi.

| Konfiguraatio | kuvaus |
|---|---|
| Päivämäärästä/Päivämäärään| Päivämääräalue, jolle hintaraportti luodaan. Kesto on tällä hetkellä enintään 7 päivää. |
| Kanava| Myymälä, jolle hintaraportti luodaan. |
| Näytä tuotteet, joita on varastossa| Kun asetukseksi valitaan **Kyllä**, vain niiden tuotteiden hinnat näytetään, joita on tällä hetkellä myymälän fyysisessä varastossa. |
| Näytä versioiden hinnat | Kun asetukseksi valitaan **Kyllä**, versioiden hinnat näytetään päätuotteiden ohella. Tämä asetus **otetaan käyttöön** vain, jos käytössä versiokohtaisia hintoja, koska muutoin rivejä on erittäin paljon. Tulevissa versioissa otetaan käyttöön dimensiopohjaiset hinnat, jolloin myymäläpäällikkö voi valita dimensiot, joiden hinnat näytetään. |
| Näytä tuotteet, joilla on hintamuutoksia | Kun asetukseksi valitaan **Kyllä**, vain niiden päivämäärien hinnat näytetään, jolloin hintaa on muutettu. Valitun **Päivämäärästä**-kentän *yhtä päivää aikaisempi* hinta on aina näkyvissä, jotta myymäläpäällikön on helppo havaita tuotteet, joiden hinta ei ole muuttunut koko valittuna ajanjaksona. Tällä tavoin hän näkee myös nykyisen hinnan. |

Raportin luonnin jälkeen Excel-tiedosto voidaan ladata mahdollista lisäsuodatusta varten. Hintaraportin avulla voidaan tarkistaa myös tuotteiden aiempien päivämäärien historialliset hinnat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
