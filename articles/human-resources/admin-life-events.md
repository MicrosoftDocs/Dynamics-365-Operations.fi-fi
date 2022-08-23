---
title: Järjestelmänvalvojan oikeuksien asettaminen elinkaaritapahtumille
description: Tässä artikkelissa kerrotaan, miten järjestelmänvalvojan oikeuksia voidaan määrittää elinkaaritapahtumille Microsoft Dynamics 365 Human Resourcesissa.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229897"
---
# <a name="set-administrator-rights-for-life-events"></a>Järjestelmänvalvojan oikeuksien asettaminen elinkaaritapahtumille

[!include [banner](../includes/preview-banner.md)]

Järjestelmänvalvojat voivat päivittää elinkaaritapahtuma-asetuksia konfigurointiasetusten mukaan. **Henkilöstöhallinnan parametrit** -sivulla voit määrittää parametreja, joiden avulla järjestelmänvalvojat voivat tehdä muutoksia suunnitelman valintaan. Voit myös estää järjestelmänvalvojia tekemästä muutoksia.

**Henkilöstöhallinnan parametrit** -sivulla voit määrittää suunnitelmien muutosrajoitukset vahvistetuille suunnitelmille ja elinkaaritapahtuman asetuksille.

Jos **Vahvistetut suunnitelmat** -vaihtoehto on valittuna, muutoksia voi tehdä vain, jos rekisteröintikausi on aktiivinen. (Esimerkkejä rekisteröintikausista ovat avoimet rekisteröintikaudet, uuden työntekijät rekisteröintikauden ja elinkaaritapahtuman rekisteröintikaudet.) Jos tätä vaihtoehtoa ei ole valittu, voit tehdä muutoksia milloin tahansa.

Jos **Elinkaaritapahtuman vaihtoehdot** -kohta on valittuna, suunnitelmaan tehdyt muutokset elinkaaritapahtuman aikana rajoittuvat elinkaaritapahtuman vaihtoehtoihin, jotka on määritetty suunnitelmatyypissä. Jos tätä vaihtoehtoa ei ole valittu, suunnitelman valintoja voi muuttaa elinkaaritapahtuman aikana.

## <a name="set-plan-change-restrictions"></a>Suunnitelman muutosrajoitusten asettaminen

**Henkilöstöhallinnan parametrit** -sivun **Etujen hallinta** -välilehdessä ovat käytettävissä seuraavat kentät.

| Kenttä | Kuvaus |
|-------|-------------|
| Vahvistetut suunnitelmat | Valitse tämä vaihtoehto, jos suunnitelmaa koskevat muutokset ovat sallittuja vain, jos rekisteröintikausi on aktiivinen. Jos tätä vaihtoehtoa ei ole valittu, voit tehdä muutoksia milloin tahansa. |
| Elinkaaritapahtuman vaihtoehdot | Valitse tämä vaihtoehto, jos suunnitelmaan tehdyt muutokset elinkaaritapahtuman aikana rajoittuvat elinkaaritapahtuman vaihtoehtoihin, jotka on määritetty suunnitelmatyypissä. Jos tätä vaihtoehtoa ei ole valittu, suunnitelman valintoja voi muuttaa elinkaaritapahtuman aikana. |
