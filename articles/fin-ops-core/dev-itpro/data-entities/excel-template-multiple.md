---
title: Useita laskentataulukoita sisältävät tietomallit
description: Tässä ohjeaiheessa käsitellään tietojen tuontia Finance and Operationsiin Excelin tietoyksikkömallien avulla.
author: peakerbl
ms.date: 01/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: cf3c423bdf06685a3c4025551927123773ae818a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070058"
---
# <a name="data-templates-with-multiple-worksheets"></a>Useita laskentataulukoita sisältävät tietomallit

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Sovelluksen tietojen hallinta tukee tietoyksiköiden Microsoft Excel -pohjaisia malleja. Näissä malleissa voi olla yksi laskentataulukko tai useita laskentataulukkoja. Useita laskentataulukkoja sisältäviä malleja käytetään usein, kun tietoja halutaan hallita yhdessä tiedostossa, joka voidaan vielä useisiin tietoyksiköihin. Esimerkki: toimipaikat ja varastot.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Kerran ladatun tiedoston yhdistämiseen kaikkiin yksiköihin
Esimerkkinä voisi olla tilanne, jossa yhdessä Excel-tiedostossa on **Toimipaikat**- ja **Varastot**-nimiset laskentataulukot. Voit määrittää tietojen tuontiprojektin lisäämällä ensimmäisen tietoyksikön, **Toimipaikat**, lataamalla tiedosto sitten. Voit valita **Toimipaikat** tässä yksikössä käytettäväksi laskentataulukoksi.

Jos lisäät toisen yksikön, **Varastot**, lähtemättä **Lisää tiedosto** -lomakkeesta, laskentataulukkohaku antaa valita **Varasto**-laskentataulukon ilman, että tiedosto on ladattava uudelleen. Uusi tiedosto tarvitsisi ladata vain, jos **Varastot**-tiedot olisivat eri tiedostossa.

![Useita laskentataulukoita.](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>Laskentataulukon korjaaminen yksikön yhdistämismääritykseen

Laskentataulukon yhdistämismääritys tuontityön tietoyksikköön voidaan korjata ruudukossa. Ruudukon **Laskentataulukko**-sarake sisältää yhdistetyn tiedoston laskentataulukot. Voit valita toisen laskentataulukon avattavasta valikosta. Jos valittu laskentataulukko on jo yhdistetty yksikköön tietoprojektissa, järjestelmä pyytää vahvistamaan muutoksen. Kaikki yhdistämismääritykset kannattaa korjata ruudukossa.

![Laskentataulukon yhdistämismäärityksen päivitys.](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Uudelleenyhdistäminen uuteen tiedostoon

Jos saman tiedoston uusi versio tai täysin uusi tiedosto on ladattava tietoprojektin aiemmin luotuihin yksiköihin, on käytettävä **Lisää tiedosto** -vaihtoehtoa ja yksiköt on lisättävä uudelleen aivan kuin ne lisättäisiin ensimmäisen kerran. Järjestelmä vahvistaa ennen jatkamista, että haluat korvata tietoprojektin aiemmin luodut yksiköt. Yksiköt, joita ei ole lisätty uudelleen (tai korjattu), sisältävät edelleen edellisestä tiedostosta tehdyt aiemmat yhdistämismääritykset.

## <a name="upload-a-file-using-run-project"></a>Tiedoston lataaminen Suorita projekti -toiminnolla

Voit ladata Excel-tiedoston samalla, kun tuot projektin **Suorita projektit** -asetuksella. Ole huolellinen ja lataa vain tiedostot, joissa on samat laskentataulukot kuin tietoprojektin tietoyksiköiden aiemmin luoduissa yhdistämismäärityksissä. Jos laskentataulukkoa ei ole juuri ladatussa tiedostossa, järjestelmä ilmoittaa virheestä ja lopettaa tuonnin. Jos yhdistämistä laskentataulukkoon on muutettava yksikössä, tietoprojektin yhdistämismääritykset on ensin päivitettävä tietoprojektissa ennen **Suorita projekti** -toiminnon käyttöä tiedostossa.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
