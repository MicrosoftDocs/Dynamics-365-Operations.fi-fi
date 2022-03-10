---
title: Varasto-oikaisu
description: Tässä aiheessa on tietoja varaston oikaisun kirjauskansiosta ja käsittelystä, kun käytät scale uniteja.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 3999c16cdf4fce342ce56ca3a459944566c6d0cb6a8460d30d2254356e5cba82
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748808"
---
# <a name="warehouse-inventory-adjustment"></a>Varasto-oikaisu

[!include [banner](../includes/banner.md)]

Varaston oikaisuominaisuutta käytetään, kun suoritetaan pilvi- ja reunapalvelujen scale uniteja [valmistuksen kuormituksille](cloud-edge-workload-manufacturing.md) ja [varaston hallinnan kuormituksille](cloud-edge-workload-warehousing.md).

Kun työntekijä tekee varaston oikaisun varastosovelluksen avulla scale unitin varastonhallinnan kuormitusta vasten, fyysisen käytettävissä olevan päivityksen käsittelee **Varaston oikaisun kirjauskansio** -erätyö, joka suoritetaan ja ajoitetaan valitsemalla **Varastonhallinta > Kausittaiset tehtävät > Varaston oikaisun kirjauskansio**.

Seuraavissa varastosovellusten työprosesseissa käytetään tällä hetkellä **Varaston oikaisun kirjauskansiota** scale unit -kuormituksissa:

- Oikaisu sisään/ulos
- Inventointi
- Rekisterikilven lataus

Useita varaston tapahtumia luodaan osana kutakin varaston oikaisuprosessia, koska keskuksen ja scale unitin käyttöönotot jakavat varastotietueet.

## <a name="inventory-adjustment-example"></a>Varaston oikaisun esimerkki

Tässä esimerkissä varastotyöntekijä on rekisteröinyt varastosovelluksen avulla käytettävissä olevan varaston lisäämisen.

Ensin scale unitin kuormitus luo positiiviselle fyysiselle oikaisulle varaston oikaisutapahtuman, joka tämän jälkeen synkronoidaan keskukseen ja mikä johtaa keskuksen käytettävissä olevan varaston suurenemiseen.

| Laji                                    | Skaalausyksikkö | Siirtosuunta | Keskus |
|-----------------------------------------|------------|-----------|-----|
| Varasto-oikaisu          | +1         | ->        | +1  |

Tämän jälkeen keskus käsittelee inventoinnin kirjauskansion kirjauksen, joka vastaanotetaan [sanoman käsittelijän sanomien](cloud-edge-message-processor-messages.md) kautta. Tämä päivittää käytettävissä olevan lisävaraston. Jotta käytettävissä ei olisi kaksinkertaista varastoa, keskus luo vastatapahtuman prosessin osana ja poistaa varaston oikaisuun liittyvän aiemmin tallennetun käytettävissä olevan varaston.

| Laji                                    | Skaalausyksikkö | Siirtosuunta | Keskus |
|-----------------------------------------|------------|-----------|-----|
| Inventointi                                | +1         | <-        | +1  |
| Varaston oikaisu (vastakirjaus) | -1         | <-        | -1  |

Kun asteikkoyksikkö on luonut **Varaston oikaisun kirjauskansion** keskuksessa, näkyvissä on sekä **Inventointikirjauskansio** että **Vastakirjauskansio**, jotka keskus luo osana oikaisuprosessia.

Noudattamalla seuraavia ohjeita voit tarkastella kaikkia näitä kirjauskansiomerkintöjä ja tapahtumia Supply Chain Managementissa:

1. Kirjautuu scale unitiin.
1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Varaston oikaisun kirjauskansio**.
1. **Varaston oikaisun kirjauskansio** -sivulla etsi ja avaa kirjauskansio, joka kirjasi käytettävissä olevan varaston muutoksen. **Kirjauskansion rivit** -osassa näkyvät kaikki tämän kirjauskansion kirjaamat oikaisut.
1. Kirjaudu sisään keskukseen.
1. Siirry kohtaan **Varastonhallinta \> Kausittaiset tehtävät \> Varaston oikaisun kirjauskansio**.
1. **Varaston oikaisun kirjauskansio** -sivulla pitäisi näkyä sama kirjauskasio, jos keskus ja scale unit on synkronoitu.
1. Avaa kirjauskansio. Jos [sanoman käsittelijän sanomat](cloud-edge-message-processor-messages.md) on käsitelty, näkyvissä ovat linkit otsikon kohtiin **Inventointikirjauskansio** ja **Vastakirjauskansio**.
    - **Inventointikirjauskansiossa** tulisi näkyä samat dimensioarvot kuin kirjauskansion riveillä.
    - **Vastakirjauskansiossa** tulisi näkyä vastakirjaus, joka poistaa kaksoisvarasto-oikaisun.
    > [!NOTE]
    > Kun kaikki synkronointi ja käsittely on tehty, **Inventointikirjauskansio** ja **Vastakirjauskansio** synkronoidaan takaisin skaalausyksikköön. Voit tarkastella niitä myös asianmukaisella **Varaston oikaisun kirjauskansio** -sivulla.
