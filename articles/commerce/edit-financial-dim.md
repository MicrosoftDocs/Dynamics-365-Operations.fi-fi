---
title: Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen
description: Tässä artikkelissa kerrotaan, miten vähittäismyyntitapahtumien taloushallinnon dimensioita muokataan Microsoft Dynamics 365 Commercessa.
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.industry: Retail
ms.openlocfilehash: b382907cd79a13319601dd694261319875565947
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268391"
---
# <a name="edit-financial-dimensions-for-retail-transactions"></a>Vähittäismyyntitapahtumien taloushallinnon dimensioiden muokkaaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kerrotaan, miten vähittäismyyntitapahtumien taloushallinnon dimensioita muokataan Microsoft Dynamics 365 Commercessa.

## <a name="edit-financial-dimensions"></a>Taloushallinnon dimensioiden muokkaaminen

Voit muokata vähittäismyyntitapahtumien taloushallinnon dimensioita Commerce-pääkonttorisovelluksessa seuraamalla alla olevia ohjeita.

1. Avaa **Integrointisovellusten taloushallinnon dimension määritykset** -sivu.
1. Valitse aktiivinen **Oletusdimensioiden integrointi** -tietue.
1. Varmista **Taloushallinnon dimensiot** -pikavälilehdessä, että Excel-laskentataulukon kaikki muokattavat dimensiot löytyvät **Valitut**-luettelosta. Lisätietoja on kohdassa [Tietoentiteetit](../fin-ops-core/dev-itpro/financial/financial-dimension-configuration-integration.md#data-entities).
1. Lataa ja avaa Excel-tiedosto **Laskelmat**-sivulla, **Vähittäismyyntitapahtumat**-sivulla tai **Tapahtuman tarkistusvirheet** -ruudussa **Myymälän taloustiedot** -työtilassa.
1. Jos haluat muuttaa tapahtuman taloushallinnon dimensiota, valitse **Rakenne** ja valitse sitten **Tapahtuma (tarkistettavissa)** -rivin vieressä oleva kynäsymboli.
1. Etsi ja valitse **FinancialDimensionDisplayValue**-kenttä, valitse Excel-laskentataulukon otsikon osan solu ja valitse sitten **Lisää selite**.
1. Valitse edellisessä vaiheessa valitun solun alla oleva solu. Valitse **Lisää arvo** ja valitse sitten **Päivitä**. Taloushallinnon dimensiot lisätään Excel-laskentataulukkoon, ja niitä voi muokata ja julkaista.
1. Voit muuttaa tapahtumarivien dimensioita valitsemalla **Myyntitapahtumat (tarkistettavissa)** -rivin, valitsemalla sitten kynäsymbolin ja toistamalla vaiheet 6 ja 7.
1. Voit muuttaa maksurivien dimensioita valitsemalla **Maksutapahtumat (tarkistettavissa)** -rivin, valitsemalla sitten kynäsymbolin ja toistamalla vaiheet 6 ja 7.

## <a name="additional-resources"></a>Lisäresurssit

[Kassanhallinnan ja itsepalvelutukun hallintatapahtumien muokkaaminen ja tarkastaminen](edit-cash-trans.md)

[Online-tilauksen ja asynkronisten asiakastilausten tapahtumien muokkaaminen ja tarkistaminen](edit-order-trans.md)

[Excel-työkirjan luominen vähittäismyyntitapahtumien muokkaamista varten](create-excel-edit.md)

[Kenttien lisääminen Excel-työkirjaan vähittäismyyntitapahtumien muokkaamista varten](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
