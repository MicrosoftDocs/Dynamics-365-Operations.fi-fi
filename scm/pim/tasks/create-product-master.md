--- 
title: "Luo päätuote"
description: "Luo ennalta määritetyille varianteille päätuotteen."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: b783c41459163ab5a0644a1ff5c39b6933bcdb1b
ms.contentlocale: fi-fi
ms.lasthandoff: 07/28/2017

---
# <a name="create-a-product-master"></a>Luo päätuote

[!include[task guide banner](../../includes/task-guide-banner.md)]

Luo ennalta määritetyille varianteille päätuotteen. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF. Tämä menettely on tarkoitettu tuotesuunnittelijalle.


## <a name="create-a-new-product-master"></a>Luo uusi päätuote
1. Siirry kohtaan Tuotetietojen hallinta > Tuotteet > Päätuotteet.
2. Valitse Uusi.
3. Kirjoita arvo Tuotenumero-kenttään.
    * Numeron tulee olla yksilöivä. Tuotetunnus-kentälle voidaan määrittää numerojärjestys. Tällöin käyttäjän ei tarvitse syöttää arvoa.  
4. Kirjoita arvo Tuotteen nimi -kenttään.
    * Syötä kuvaava tuotteen nimi. Arvo saa oletusarvon haun nimestä, mutta käyttäjä voi muuttaa arvon.  
5. Avaa haku valitsemalla Tuotedimensioryhmä-kentässä avattavan valikon painike.
    * Tuotedimensioryhmä määrittää, mitä neljää tuotedimensiota tuotevarianttien luomisessa voidaan käyttää. Tässä esimerkissä käytetään ryhmää, joka sisältää värin ja koon.  
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
    * Oletusmääritysmenetelmä on Ennalta määritetty variantti. Tässä esimerkissä käytetään sitä.  
8. Valitse OK.

## <a name="select-product-dimension-groups"></a>Tuotedimensioryhmien valitseminen
1. Avaa haku valitsemalla Väriryhmä-kentässä avattavan valikon painike.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
4. Avaa haku valitsemalla Kokoryhmä-kentässä avattavan valikon painike.
5. Etsi haluamasi tietue luettelosta ja valitse se.
6. Napsauta luettelossa valitulla rivillä olevaa linkkiä.

## <a name="add-dimension-groups"></a>Lisää dimensioryhmät
1. Valitse toimintoruudussa Tuote.
2. Avaa valintaikkunalomake valitsemalla Dimensioryhmät.
3. Avaa haku valitsemalla Varastodimensioryhmä-kentässä avattavan valikon painike.
    * Varastodimensioilla hallitaan nimikkeiden tallentamista varastoon ja ottamista sieltä. Varastodimensio voi sisältää esimerkiksi toimipisteen ja varaston.  
4. Etsi haluamasi tietue luettelosta ja valitse se.
5. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
6. Avaa haku valitsemalla Seurantadimensioryhmä-kentässä avattavan valikon painike.
    * Seurantadimensioryhmä määrittää, mitkä seurantadimensiot voit tuotteelle määrittää. Esimerkiksi eränumeroa ja sarjanumeroa voidaan käyttää varastonimikkeiden seurantaan.  
7. Etsi haluamasi tietue luettelosta ja valitse se.
8. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
9. Valitse OK.
10. Valitse Tallenna.
11. Sulje sivu.

