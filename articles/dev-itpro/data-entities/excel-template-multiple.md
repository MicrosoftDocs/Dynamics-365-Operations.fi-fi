---
title: "Tietojen tuonti useita laskentataulukkoja sisältävistä Excelin tietoyksikkömalleista"
description: "Tässä aiheessa käsitellään tietojen tuontia Excelin tietoyksikkömallien avulla Microsoft Dynamics 365 for Finance and Operations, Enterprise editioniin."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 84b9e9128d7ea6cdf9949549f4ab7a1c6c01691b
ms.contentlocale: fi-fi
ms.lasthandoff: 12/14/2017

---

# <a name="excel-templates-with-multiple-worksheets"></a>Useita laskentataulukkoja sisältävät Excel-mallit

Microsoft Dynamics 365 for Finance and Operations, Enterprise editionin tietojen hallinta tukee Microsoft Excel -pohjaisia tietoyksikkömalleja. Näissä malleissa voi olla yksi laskentataulukko tai useita laskentataulukkoja. Useita laskentataulukkoja sisältäviä malleja käytetään usein, kun tietoja halutaan hallita yhdessä tiedostossa, joka voidaan vielä useisiin tietoyksiköihin. Esimerkki: toimipaikat ja varastot.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Kerran ladatun tiedoston yhdistämiseen kaikkiin yksiköihin
Esimerkkinä voisi olla tilanne, jossa yhdessä Excel-tiedostossa on **Toimipaikat**- ja **Varastot**-nimiset laskentataulukot. Voit määrittää tietojen tuontiprojektin lisäämällä ensimmäisen tietoyksikön, **Toimipaikat**, lataamalla tiedosto sitten. Voit valita **Toimipaikat** tässä yksikössä käytettäväksi laskentataulukoksi.

Jos lisäät toisen yksikön, **Varastot**, lähtemättä **Lisää tiedosto** -lomakkeesta, laskentataulukkohaku antaa valita **Varasto**-laskentataulukon ilman, että tiedosto on ladattava uudelleen. Uusi tiedosto tarvitsisi ladata vain, jos **Varastot**-tiedot olisivat eri tiedostossa.

![Useita laskentataulukoita](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a>Laskentataulukon korjaaminen yksikön yhdistämismääritykseen

Laskentataulukon yhdistämismääritys tuontityön tietoyksikköön voidaan korjata ruudukossa. Ruudukon **Laskentataulukko**-sarake sisältää yhdistetyn tiedoston laskentataulukot. Voit valita toisen laskentataulukon avattavasta valikosta. Jos valittu laskentataulukko on jo yhdistetty yksikköön tietoprojektissa, järjestelmä pyytää vahvistamaan muutoksen. Kaikki yhdistämismääritykset kannattaa korjata ruudukossa.

![Laskentataulukon yhdistämispäivityksen päivitys](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Uudelleenyhdistäminen uuteen tiedostoon

Jos saman tiedoston uusi versio tai täysin uusi tiedosto on ladattava tietoprojektin aiemmin luotuihin yksiköihin, on käytettävä **Lisää tiedosto** -vaihtoehtoa ja yksiköt on lisättävä uudelleen aivan kuin ne lisättäisiin ensimmäisen kerran. Järjestelmä vahvistaa ennen jatkamista, että haluat korvata tietoprojektin aiemmin luodut yksiköt. Yksiköt, joita ei ole lisätty uudelleen (tai korjattu), sisältävät edelleen edellisestä tiedostosta tehdyt aiemmat yhdistämismääritykset.

## <a name="upload-a-file-using-run-project"></a>Tiedoston lataaminen Suorita projekti -toiminnolla

Voit ladata Excel-tiedoston samalla, kun tuot projektin **Suorita projektit** -asetuksella. Ole huolellinen ja lataa vain tiedostot, joissa on samat laskentataulukot kuin tietoprojektin tietoyksiköiden aiemmin luoduissa yhdistämismäärityksissä. Jos laskentataulukkoa ei ole juuri ladatussa tiedostossa, järjestelmä ilmoittaa virheestä ja lopettaa tuonnin. Jos yhdistämistä laskentataulukkoon on muutettava yksikössä, tietoprojektin yhdistämismääritykset on ensin päivitettävä tietoprojektissa ennen **Suorita projekti** -toiminnon käyttöä tiedostossa.


