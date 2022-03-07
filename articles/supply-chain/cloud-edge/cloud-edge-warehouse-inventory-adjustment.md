---
title: Varasto-oikaisu
description: Tässä aiheessa on tietoja varaston oikaisun kirjauskansiosta ja käsittelystä, kun käytät scale uniteja.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938223"
---
# <a name="warehouse-inventory-adjustment"></a>Varasto-oikaisu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Varaston oikaisuominaisuutta käytetään, kun suoritetaan pilvi- ja reunapalvelujen scale uniteja [valmistuksen kuormituksille](cloud-edge-workload-manufacturing.md) ja [varaston hallinnan kuormituksille](cloud-edge-workload-warehousing.md).

Kun työntekijä tekee varaston oikaisun varastosovelluksen avulla scale unitin varastonhallinnan kuormitusta vasten, fyysisen käytettävissä olevan päivityksen käsittelee **Varaston oikaisun kirjauskansio** -erätyö, joka suoritetaan ja ajoitetaan valitsemalla **Varastonhallinta > Kausittaiset tehtävät > Varaston oikaisun kirjauskansio**.

Seuraavissa varastosovellusten työprosesseissa käytetään tällä hetkellä **Varaston oikaisun kirjauskansiota** scale unit -kuormituksissa:

- Oikaisu sisään/ulos
- Inventointi
- Rekisterikilven lataus

Useita varaston tapahtumia luodaan osana pilvi- ja reunapalvelun varaston oikaisuprosessia, koska keskuksen ja scale unitin käyttöönotot jakavat varastotietueet.

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
