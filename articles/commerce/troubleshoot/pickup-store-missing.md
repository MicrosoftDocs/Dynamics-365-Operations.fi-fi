---
title: Vähittäismyymälä ei näy noutomyymälöiden luettelossa
description: Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun vähittäismyyntiliike ei ole luettelossa myymälöistä, joista nimikkeitä voi noutaa.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 652f5f1a779a412c21c18814071ba0fb7dd2e155
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585310"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Vähittäismyymälä ei näy noutomyymälöiden luettelossa

[!include [banner](../../includes/banner.md)]

Tämä ohjeaihe antaa vianmääritysohjeet, jotka voivat auttaa, kun vähittäismyyntiliike ei ole luettelossa myymälöistä, joista nimikkeitä voi noutaa.

## <a name="description"></a>kuvaus

Vähittäismyyntiliike ei näy myymälöiden luettelossa, joista nimikkeitä voi noutaa.

## <a name="resolution"></a>Ratkaisu

### <a name="configure-the-longitude-and-latitude-for-the-store-address-in-commerce-headquarters"></a>Myymälän osoitteen pituus- ja leveysasteen konfiguroiminen Commerce headquarters -sovelluksessa

Myymälän osoitteen pituus- ja leveysasteen konfiguroimisen Commerce headquarters -sovelluksessa voit tehdä seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavat \> Myymälät \> Kaikki myymälät**.
1. Etsi myymälä, jonka haluat näkyvän noutovaihtoehdoissa sähköisen kaupankäynnin sivustossa. Merkitse sen **Toimintayksikön numero** -arvo muistiin.
1. Valitse **Organisaation hallinto \> Organisaatiot \> Toimintayksiköt**.
1. Hae aiemmin muistiin merkittyä toimintayksikön numeroa ja valitse sitten toimintayksikkö hakutuloksista.
1. Valitse **Osoitteet**-pikavälilehdessä **Lisää vaihtoehtoja** ja valitse sitten **Lisäasetukset**.
1. Varmista **Yleiset**-pikavälilehdessä, että **Pituuaste**- ja **Leveysaste**-kentät on määritetty oikein. Varmista osana tätä vaihetta, että arvot on määritetty oikein positiivisiksi tai negatiivisiksi luvuiksi.

### <a name="configure-fulfillment-groups-in-commerce-headquarters"></a>Täydennysryhmien konfiguroiminen Commerce headquarters -sovelluksessa

Voit määrittää täydennysryhmät Commerce headquarters -sovelluksessa seuraavasti.

1. Valitse **Retail ja Commerce \> Kanavat \> Verkkokaupat**.
1. Valitse määritettävä verkkokauppa.
1. Valitse toimintoruudussa ensin **Asetukset** ja sitten **Täytäntöönpanoryhmän määritys**.
1. Valitse **Täytäntöönpanoryhmän määritys** -sivulla verkkokaupan täytäntöönpanoryhmä.
1. Varmista **Asetukset**-kohdasta, että vähittäiskauppa on määritetty oikein täytääntöpanoryhmälle.

## <a name="additional-resources"></a>Lisäresurssit 

[Toimintayksikön luominen](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit)

[Online-kanavan määrittäminen](../channel-setup-online.md)
