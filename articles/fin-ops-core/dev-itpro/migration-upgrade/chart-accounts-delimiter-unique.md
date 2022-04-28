---
title: Tilikartan erottimen muuttaminen yksilöiväksi
description: Tässä ohjeaiheessa selitetään, minkä vuoksi tilikartan ja dimension arvoilla ei voi olla sama erotin. Erotinarvot on muutettava päivityksen jälkeen.
author: panolte
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6081a62077f1fc6b6920991ed6faae667c25a47c
ms.sourcegitcommit: e8a2a1e34fa48a42afac9724828f4ec72b6d7085
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/13/2022
ms.locfileid: "8573615"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Tilikartan erottimen muuttaminen yksilöiväksi

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2012:ssä tilikartan ja dimension arvoissa olisi mahdollista käyttää samaa erotinta. Tilikartan ja dimension nimillä tai arvoilla ei voi olla talous- ja toimintosovellusten nykyisissä versioissa sama erotin. Jos samaa erotinta käytetään kahdesti, voit muuttaa sen päivityksen jälkeen. 

## <a name="update-delimiter"></a>Erottimen päivitys
Jos tilikartan kanssa on ristiriita, tilikartan erotin ja projektin tai aliprojektin tunnuksen muoto voidaan muuttaa. Muita dimension erottimia ei voi muuttaa. 
- Voit muuttaa tilikartan erottimen tehdyn päivityksen jälkeen valitsemalla **Kirjanpitoparametrit** > **Tilikartta ja dimensiot** > **Muuta erotinta**. 
- Jos ainoa ristiriita on projektin tai aliprojektin tunnuksen muodon kanssa, voit vaihtaa kyseisen arvon valitsemalla **Projektinhallinnan ja kirjanpidon parametrit** > **Yleiset** > **Muuta aliprojektin muotoa**. 

### <a name="other-considerations"></a>Muuta huomioon otettavaa
Kuten projekti-/aliprojektitunnuksella, muilla taloushallinnon dimensioissa, kuten toimittajissa tai asiakkaissa, käytetyillä perustietotietueilla ei saa olla samaa merkkiä kuin tilikartan erottimena. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Erottimen päivitystarpeen määrittäminen ympäristössä 
Jos päivitetyn ympäristön erottimissa on ristiriita, arvojen kirjaamisessa voi esiintyä epävakautta segmentoidussa kirjauksen hallinnassa tai dimensiomerkinnän ohjauksessa. Tämä tarkoittaa sitä, sinun on aina käytettävä hakuja tai lisätietoikkunaa, kun kirjaat tili- ja dimensioyhdistelmiä.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
