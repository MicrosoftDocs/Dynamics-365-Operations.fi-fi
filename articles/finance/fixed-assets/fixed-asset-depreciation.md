---
title: Käyttöomaisuuden poisto
description: Tämä ohjeaihe sisältää käyttöomaisuuden poiston yleiskatsauksen.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus, AssetBookTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b399ab3df9bddbce8b96752ef344bf93cb2563c
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969100"
---
# <a name="fixed-asset-depreciation"></a>Käyttöomaisuuden poisto

[!include [banner](../includes/banner.md)]

Tämä ohjeaihe sisältää käyttöomaisuuden poiston yleiskatsauksen.

Poisto on kausittainen tapahtuma, joka yleensä vähentää käyttöomaisuuserän tasearvoa ja kirjataan kuluksi tulostilille. Tämän vuoksi päätiliä käytetään yleensä taseen kausittaisen poiston hyvittämiseen. Vastatili on tilikartan tuloslaskelmaosaan kuuluva tili.

## <a name="depreciation-adjustment"></a>Poistojen oikaisu
Poiston oikaisuksi kirjataan yleensä vain aiemmin kirjatun poistotapahtuman korjaus. Siksi sekä pää- että vastatili määritetään samaan tapaan kuin poistoissa käytettävät tilit. Poistojen oikaisun summa voi olla positiivinen tai negatiivinen, mutta päätili (tasetilinä) ja vastatili (yleensä tulostilinä) toimivat samaan tapaan.

## <a name="extraordinary-depreciation"></a>Erikoispoisto
Erikoispoisto toimii samalla tavoin kuin peruspoisto. Poistosumma hyvitetään taseeseen ja käyttöomaisuuserän arvoa vähennetään päätilin avulla. Vastatili on tulostili, jolle tilikaudelta laskettu poisto kirjataan kuluna. 

Erikoispoisto toimii peruspoistosta riippumatta. Koska erikoispoisto on erillinen tapahtumatyyppi, se voidaan kirjata ja raportoida tavallisesta poistosta erillisenä tapahtumana.

## <a name="special-depreciation-allowance"></a>Erityinen poistovähennys
Erityisillä poistovähennyksillä voidaan tehdä ylimääräisiä poistoja sinä vuonna, jona käyttöomaisuuserä otetaan käyttöön ja siitä tehdään poisto ensimmäistä kertaa. Erityiset poistovähennykset on suoritettava ennen muiden poistojen laskemista. Koska erityiset poistovähennykset tunnistetaan yleensä vasta myöhemmin käyttöomaisuuserän käyttöiän aikana, kannattaa käyttää tämäntyyppiseen poistoon kirjaa, jota ei kirjata kirjanpitoon. Voit käyttää kausittaista Poista kirjanpitoon kirjaamattomat tapahtumat -toimintoa ja poistaa aiempia tapahtumia näistä kirjoista. Voit sitten poistaa poistohistorian kiinteän käyttöomaisuuden kirjasta, kirjata erityisen poiston, kun se on tunnistettu, ja kirjata jäljellä olevat vuoden poistotapahtumat. 

Erityisten poistovähennysten tietueita voidaan luoda rajattomasti. Kun tietueet on määritetty käyttöomaisuusryhmän kirjaan, niitä käytetään käyttöomaisuuserän poistokirjassa. 

Erityiset poistovähennykset kirjataan prosenttina tai kiinteänä summana. Erityisiä poistovähennyksiä kirjattaessa tapahtumat kirjataan kirjaan poistotapahtumista erillisinä tapahtumina.

## <a name="depreciation-calendars"></a> Poistokalenterit
Jokaisessa kirjassa on kalenteri, jota käytetään käyttöomaisuuden poistoissa. Kirja käyttää oletuksena kirjanpidon vuosikalenteria, jos kalenteria ei määritetä kirjassa. Kirjalle on valittava kirjanpidon vuosikalenteri, kun kirjaan liitetty poistoprofiili käyttää kirjanpidollista poistovuotta. 

Voit luoda yhteisiä kalentereita **Kirjanpidon kalenterit** -sivulla Kirjanpito-osiossa.

Lisätietoja on kohdassa [Poistomenetelmät ja -käytännöt](depreciation-methods-conventions.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]