---
title: Tuoterakenneversion hajottaminen
description: Tässä artikkelissa kuvataan pääsuunnittelun skenaario, johon liittyy tuoterakenteen version hajotus.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 17e5d8638dc02d92a0c67364790353833551250f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187407"
---
# <a name="explosion-of-a-bom-version"></a>Tuoterakenneversion hajottaminen

[!include [banner](../includes/banner.md)]

Tässä artikkelissa kuvataan pääsuunnittelun skenaario, johon liittyy tuoterakenteen version hajotus.

Tuoterakenneversion kysynnän hajotus luo kysynnän kullekin tuoterakennerivin nimikkeelle määritetyssä toimipaikassa ja mahdollisesti tietyssä varastossa. Toimipaikkakohtaisen tuoterakenteen kullekin tuoterakenneriville voidaan määrittää tietty varasto. Lisäksi kunkin tuoterakennerivin nimikkeen dimensioasetukset määrittävät, onko varasto tarpeen. Kunkin tuoterakennerivin nimikkeen tuloksena syntyvä kysyntä muodostaa jatkossa aloituspisteen lisäkysynnän hajotukselle. Tämä pääsuunnitteluskenaario sisältää seuraavat ehdot:

-   Toimipaikkadimensio on pakollinen ja se on määritettävä tarvetapahtumalle.
-   Toimipaikkadimensio on yhdenmukainen. Näin ollen alemman tason tarpeen toimipaikka on sama kuin alkuperäisen tarvetapahtuman toimipaikka.

Seuraava kuva ilmaisee, miten pääsuunnittelun kysynnän hajotus etenee. ![Kysynnän hajottaminen tuoterakenneversion avulla](./media/multisitedemandexplosionscenariousingbomversion.gif)

## <a name="additional-resources"></a>Lisäresurssit

[Tuoterakenneversion määrittäminen](master-plan-bom-version-determined.md)

[Pääsuunnittelu ja multisite-toiminnot – yleiskatsaus](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]