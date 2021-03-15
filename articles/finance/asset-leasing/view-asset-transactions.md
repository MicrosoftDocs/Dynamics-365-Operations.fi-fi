---
title: Velka-, resurssi- ja kulutapahtumien tarkasteleminen
description: Tässä ohjeaiheessa kerrotaan, kuinka voit tarkastella vuokratun omaisuuden tapahtumia. Näihin tapahtumiin sisältyvät vuokrasopimusvelkatapahtumat ja kulutapahtumat, jotka on kirjattu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 76c7eff17df92b01317544112099e391fd05d105
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995365"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Velka-, resurssi- ja kulutapahtumien tarkasteleminen

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa kerrotaan, kuinka voit tarkastella vuokratun omaisuuden tapahtumia. Näihin tapahtumiin sisältyvät vuokrasopimusvelkatapahtumat ja kulutapahtumat, jotka on kirjattu. Velan ja käyttöoikeusomaisuuserän kirjanpitoarvoja käytetään useissa raporteissa. Niitä käytetään myös oikaisuarvojen laskemiseen.

## <a name="liability-transactions"></a>Velkatapahtumat

Voit tarkastella vuokrasopimusvelkatapahtumia valitsemalla vuokrasopimuksen **Vuokrasopimusyhteenveto**-sivulla ja valitsemalla sitten **Kirjat**, jos haluat avata vuokrasopimustietueeseen liitetyt kirjat. Kun alkuperäisen tuloutuksen jälkeen lasku tai korkokirjauskansio on kirjattu, valitse **Velkatapahtumat**.

**Velkatapahtumat**-sivulla näkyvät tapahtumat, jotka joko lisäävät tai pienentävät vuokrasopimusvelkaa. Tällä sivulla olevat negatiiviset summat edustavat hyvitystapahtumia vakiosovelluksessa. Mahdolliset korkokertymät näkyvät negatiivisina arvoina ja lisäävät vuokrasopimusvelan kokonaisarvoa. Kaikki vuokrauksen oikaisut näkyvät positiivisina tai negatiivisena arvoina vuokrasopimuskirjan luonteen ja vaikutuksen mukaan. Valitun vuokrauksen vuokrasopimusvelan tämänhetkinen nettosaldo yhteensä näkyy sivun vasemmassa alareunassa.

## <a name="asset-transactions"></a>Resurssitapahtumat

Voit tarkastella vuokrauksen resurssin tapahtumia, valitse vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla ja valitse sitten **Kirjat**, jos haluat avata vuokrasopimustietueeseen liitetyt vuokrasopimuskirjat. Valitse sitten **Resurssitapahtumat**.

**Resurssitapahtuma**-sivulla näkyvät tapahtumat, jotka joko lisäävät tai pienentävät vuokrauksen resurssia ja kumulatiivisia poistotilejä. Veloitukset näkyvät positiivisina arvoina, ja hyvitykset näytetään negatiivisina arvoina **Velkatapahtumat**-sivun tapaan. Kirjatun alkuperäisen tuloutuksen ja kumulatiivisen poiston seuraava arvo näkyvät sivun vasemmassa alareunassa resurssin saldona. 

## <a name="expenses-transactions"></a>Kulutapahtumat

Voit tarkastella vuokrauksen kulutapahtumia, valitse vuokrasopimus **Vuokrasopimusyhteenveto**-sivulla ja valitse sitten **Kirjat**, jos haluat avata vuokrasopimustietueeseen liitetyt vuokrasopimuskirjat. Valitse sitten **Kulutapahtumat**.

**Kulutapahtumat**-sivulla näkyvät kaikki vuokrasopimukseen kirjatut kulut, kuten korkokulut, poistokulut ja mahdolliset toimeenpanokustannukset.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]