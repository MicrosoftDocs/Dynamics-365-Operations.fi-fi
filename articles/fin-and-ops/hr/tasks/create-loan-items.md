--- 
title: Luo lainauskohteet
description: "Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 950237499441e7f1d5b9e3355c4bd9513ad3783e
ms.openlocfilehash: aa5824a7a56136b6d09860f2ff493359dbeab9f9
ms.contentlocale: fi-fi
ms.lasthandoff: 11/01/2017

---
# <a name="create-loan-items"></a>Luo lainauskohteet

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Lainan kohteet ovat tietueita, joiden avulla voit seurata fyysisiä yrityksen työntekijöille lainaamia kohteita, kuten puhelimia ja tietokoneita. Jokaisella fyysisellä kohteella on oltava vastaava lainan kohde. Jokaisessa lainan kohteen tietueessa tulisi kuvailla, mitä lainataan, kuka vastaa lainasta sekä aika (päivinä), jonka kohde voi olla lainassa. Voit luoda samalla useita lainan kohteita, kuten avaimia, kulkukortteja tai työpukuja. Tämän menettelyn luomisessa käytetty esittely-yritys on USMF.


## <a name="create-loan-types"></a>Lainatyyppien luominen
1. Valitse Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainatyypit.
2. Valitse Uusi.
3. Syötä arvo Lainatyyppi-kenttään.
4. Kirjoita arvo Kuvaus-kenttään.
5. Määritä, kuinka monta päivää tätä lainatyyppiä olevat nimikkeet voivat olla myöhässä. 
6. Valitse Tallenna.
7. Sulje sivu.
8. Päivitä sivu.

## <a name="create-loan-items"></a>Luo lainauskohteet
1. Valitse Henkilöstöhallinto > Työntekijät > Lainan kohteet > Lainan kohteet.
2. Valitse Luo lainan kohteita.
3. Syötä Määrä-kenttään numero.
4. Kirjoita arvo Kuvaus-kenttään.
5. Avaa haku valitsemalla Lainatyyppi-kentässä avattavan valikon painike.
6. Etsi haluamasi tietue luettelosta ja valitse se.
7. Napsauta luettelossa valitulla rivillä olevaa linkkiä.
8. Määritä, miten monta päivää kohde voi olla lainassa.
    * Lainatut välineet -sivun Suunniteltu palautus -kentän oletusarvo lasketaan lisäämällä kuluvaan päivämäärään tämä numero.  
9. Avaa haku valitsemalla Vastuuhenkilö-kentässä avattavan valikon painike.
10. Klikkaa Valitse.
11. Syötä numero Aloitusarvo-kenttään.
12. Syötä numero Väli-kenttään.
13. Syötä arvo Muoto-kenttään.
    * Jos lainan kohteen aloitusnumero on esimerkiksi 10, syötä Muoto-kenttään kaksi numeroa.  
14. Valitse OK.
15. Päivitä sivu.


