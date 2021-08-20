---
title: Virhe, kun Valmiiksi ilmoitettujen kirjauskansio on kirjattu
description: Kun kirjaat valmiiksi ilmoitettujen kirjauskansion, näyttöön tulee virhesanoma, jossa sanotaan, että tilattua määrää ei voi pienentää.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTableListPage, ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 50a11aba46519a3a81c313aa1f685d45dcf35f64b50bc921d93968efab13b7b9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750927"
---
# <a name="error-when-the-report-as-finished-journal-is-posted"></a>Virhe, kun Valmiiksi ilmoitettujen kirjauskansio on kirjattu

Tietopankin numero: 4612891

## <a name="symptoms"></a>Oireet

Kun kirjaat **Ilmoita valmiiksi** -kirjauskansion, näkyviin tulee virheilmoitus, ja näyttöön tulee seuraava virhesanoma:

> Tilattua määrää ei voi vähentää, koska Tilattu-tilassa olevia avoimia varastotapahtumia ei ole riittävästi. Nimikkeet ovat ostettuja, vastaanotettuja tai rekisteröityjä.

Tämä virhe tapahtuu vain, kun **Virhemäärä**-kenttä on määritetty **Ilmoita valmiiksi** -kirjauskansion ensimmäiselle riville ja **Hyvä määrä** -kentän arvoksi määritetään viimeinen rivi. Jos **Virhemäärä**-kenttä on määritetty viimeiselle riville, virhettä ei tapahdu.

## <a name="resolution"></a>Ratkaisu

Voit estää tämän virheen avaamalla **Tuotannonhallinnan parametrit** -sivun ja valitsemalla **Yleiset**-välilehdestä **Lisää jäljellä olevaa määrää virheen määrällä** -asetuksen arvoksi *Kyllä*.
