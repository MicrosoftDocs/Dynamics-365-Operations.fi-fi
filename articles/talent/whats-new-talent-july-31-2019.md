---
title: Dynamics 365 for Talentin uudet ja muuttuneet ominaisuudet (31.7.2019)
description: Tässä ohjeaiheessa käsitellään Microsoft Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.
author: Darinkramer
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1fffe1bd8739723294c027c174d5e959c1c6010a
ms.sourcegitcommit: 4ff8c2c2f3705d8045df66f2c4393253e05b49ed
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864576"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-july-30-2019"></a>Dynamics 365 for Talentin uudet ja muuttuneet ominaisuudet (30.7.2019)

[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään Dynamics 365 for Talentin uusia tai muuttuneita ominaisuuksia.

## <a name="changes-in-attract"></a>Attractin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Attractin ohjelmakorjauksia.

## <a name="changes-in-onboard"></a>Onboardin muutokset
Tässä julkaisussa on vähäisiä Dynamics 365 Talent: Onboardin ohjelmakorjauksia.

## <a name="changes-in-core-hr"></a>Core HR:n muutokset
Tässä osassa kuvatut muutokset koskevat koontiversiota 8.1.2409.


### <a name="region-support-for-canada-and-southeast-asia"></a>Kanadan ja Kaakkois-Aasian alueellinen tuki

Olemme iloisia, kun voimme ilmoittaa, että Kanadan ja Kaakkois-Aasian alueet ovat käytettävissä Microsoft Dynamics 365 for Talentissa 1.8.2019. Tämän muutoksen myötä voi luoda ympäristöjä Kanadan ja Aasian alueilla, ja kaikkia Talent-tietoja säilytetään yksinomaan näillä alueilla. Voit luoda ympäristön näillä uusilla alueilla valitsemalla sijainnin Uusi ympäristö -valintaikkunassa ja käyttämällä tätä ympäristöä Talentin valmisteluun LCS:ssä, kuten on kuvattu kohdassa [Talentin valmistelu](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).

Tietojen siirto muiden alueiden aiemmin luoduista projekteista Kanadan ja Aasian alueille ei tueta. Vain uusia projekteja voi valmistella näillä uusilla tuetuilla alueilla.

### <a name="new-active-positions-list-page"></a>Uudet aktiiviset toimet -luettelosivu

Toimiin perustavissa luetteloissa on nyt seuraavat vaihtoehdot: **Kaikki toimet**, **Aktiiviset toimet**, **Avoimet toimet** ja **Käytöstä poistetut toimet**. Uudella **Aktiiviset toimet** -luettelosivulla näkyvät vain nämä toimet, jotka ovat joko avoimia tai täytettyjä sekä aktiivisia kuluvana päivänä. 

### <a name="allow-course-participants-to-be-added-to-open-courses"></a>Kurssin osallistujien avoimiin kursseihin lisäämisen salliminen

Tämän viikon muutokset korjaavat ongelman, jossa vain suorat alaiset voidaan rekisteröidä avoimiin kursseihin.

### <a name="fte-analysis-displaying-incorrect-fte-number"></a>FTE-analyysissa näkyy virheellinen FTE-numero

**FTE-analyysi** on korjattu **henkilöstön hallinnan** **Analytiikka**-välilehdessä.

### <a name="final-comments-label-translation"></a>Viimeiset kommentit -selitteen käännös

**Viimeiset kommentit** -selite on nyt käännetty tarkistuslomakkeessa.

## <a name="in-preview"></a>Esiversiossa

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Esiversiotoiminnot on otettu käyttöön vain eristysympäristöissä

Voit määrittää Talentin uutta esiintymää valmisteltaessa, onko esiintymän tyyppi **Tuotanto** vai **Eristys**. **Eristys**-tyypin esiintymissä uusia toimintoja voi testata varhaisessa vaiheessa. Kaikki aiemmin luodut Talent-esiintymät päivitetään **Tuotanto**-esiintymän tyyppiin. Jos haluat, että jokin aiemmin luoduista esiintymistä päivitetään **Eristys**-esiintymätyypiksi, ota yhteyttä [tukeen](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) ja tee muutospyyntö.

Lisätietoja muutosten julkaisemisesta on kohdassa [Talentin valmistelu](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent).

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Laajennettujen suorituskykytietojen näyttäminen esimiehen itsepalvelutoiminnossa

Uuden vaihtoehdon avulla esimiehet voit tarkastella sekä suorien että epäsuorien alaisten suoriutumista. Tällä hetkellä linjapäälliköt voivat määrittää ja päivittää suorituskykytavoitteita ja antaa uusia arvioita. Lisäksi suorat esimiehet ja heidän alaisensa voivat ylläpitää ja päivittää suoritustason kirjauskansioita. Tämä auttaa varmistamaan, että kehityskeskusteluprosessi toimii sujuvasti. Kun tämä muutos otetaan käyttöön, esimiehet voivat tarkastella ja ylläpitää epäsuorien alaisten suoritustasotietoja suorien alaisten tietojen lisäksi.
