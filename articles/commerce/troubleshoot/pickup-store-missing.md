---
title: Vähittäismyymälä ei näy noutomyymälöiden luettelossa
description: Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun vähittäismyyntiliike ei ole luettelossa myymälöistä, joista nimikkeitä voi noutaa.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: b6cec3d9d598be221516506388e4797ad579a610
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286749"
---
# <a name="retail-store-doesnt-appear-in-the-list-of-stores-to-pick-up-from"></a>Vähittäismyymälä ei näy noutomyymälöiden luettelossa

[!include [banner](../../includes/banner.md)]

Tämä artikkeli antaa vianmääritysohjeet, jotka voivat auttaa, kun vähittäismyyntiliike ei ole luettelossa myymälöistä, joista nimikkeitä voi noutaa.

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

[Toimintayksikön luominen](../../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md)

[Online-kanavan määrittäminen](../channel-setup-online.md)
