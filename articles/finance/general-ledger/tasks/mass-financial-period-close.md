---
title: Tilikauden joukkosulkeminen
description: Tässä artikkelissa kuvataan, miten kausi asetetaan pitoon tai pysyvästi suljetuksi useammalle yritykselle kerralla.
author: aprilolson
ms.date: 11/16/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a85d512842b27f2d74507be16a8f2819f483e0d
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779807"
---
# <a name="mass-financial-period-close"></a>Tilikauden joukkosulkeminen

[!include [banner](../../includes/banner.md)]

Tässä artikkelissa kuvataan, miten kausi asetetaan pitoon tai pysyvästi suljetuksi useammalle yritykselle kerralla. Lisäksi tehtävässä näytetään, miten käyttäjäryhmän kirjaukset voi rajoittaa tiettyihin moduuleihin.

1. Siirry siirtymisruudussa kohtaan **Kirjanpito > Kausi suljettu > Kirjanpidon kalenterit**. 

>[!NOTE]
> Luettelossa näytettävät yritykset riippuvat sivulla valitusta vuosikalenterista. Vain valittua vuosikalenteria käyttävät yritykset näytetään.

2. Valitse **Muokkaa**.
3. Valitse kausi, jonka tilaa haluat muokata.
4. Valitse yritykset, joiden tilan haluat päivittää. Voit valita kaikki yritykset nopeasti valitsemalla valintaruudun ruudukon vasemmalla puolella.  
5. Valitse **Päivitä moduulien käyttöoikeudet** määrittääksesi tietyn moduulin kirjausoikeudet. Moduulin tilan voi myös päivittää yksitellen muokkaamalla tietueita ruudukossa. Painike on hyödyllinen, kun haluat päivittää usean yrityksen tietueet nopeasti.  
6. Valitse **Sovellus**-moduulissa päivitettävä moduuli. Klikkaa **Valitse**.
7. Valitse **Käyttöoikeustaso**-kohtaan **Kaikki**, **Ei mitään** tai tietty käyttäjäryhmä. Klikkaa **Valitse**.  
- **Kaikki** - kaikilla käyttäjillä, joilla on moduulin muokkausoikeudet, voivat tehdä kirjauksia avoimena kautena. 
- **Ei mitään** – käyttäjät eivät saa kirjata moduuliin avoimena kautena. Tietty käyttäjäryhmä ilmaisee, että vain ryhmän jäsenet voivat kirjata moduuliin avoimena kautena.  
8. Valitse **Päivitä**. 
9. Päivitä tila valitsemalla toinen kausi.
10. Valitse yritykset, joiden kauden tilan haluat päivittää.
11. Valitse **Päivitä kauden tila** ja aseta tilaksi **Pidossa**, **Avoin** tai **Suljettu pysyvästi**. **Avoin** ilmaisee, että jos käyttäjällä on käyttöoikeus, hän voi tehdä kirjauksia kauteen. **Pidossa**-tila tarkoittaa, että kaudelle ei voi tehdä kirjauksia, mutta se voidaan avata uudelleen. **Suljettu pysyvästi** -tila tarkoittaa, että kausi on suljettu, eikä sitä voi avata uudelleen. Oikaisuja ei voi kirjata. **Suljettu pysyvästi** -asetusta ei suositella, ennen kuin kaikki oikaisut ja tarkistukset ovat valmiita.  
12. Valitse **Päivitä**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
