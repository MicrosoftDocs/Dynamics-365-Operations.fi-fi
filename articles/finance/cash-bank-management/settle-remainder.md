---
title: Selvitä jäljellä olevan summa
description: Voit selvittää jäljellä olevan summan tilitystehtävästä kohdistamalla summan kirjanpitotilille.
author: mikefalkner
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 8c865b4b0481b7753588ef17bc0250bab2b6c191
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834914"
---
# <a name="settle-remainder"></a>Selvitä jäljellä olevan summa

[!include [banner](../includes/banner.md)]

Voit selvittää jäljellä olevan summan tilitystehtävästä kohdistamalla summan kirjanpitotilille tai toiselle asiakkaalle. Voit selvittää jäljellä olevan summan, kun selvität kirjauskansioon kirjattuja summia tai kun selvität vain avoimia tapahtumia.

## <a name="setting-up-defaults"></a>Oletusasetusten määrittäminen 
Ennen Selvitä jäljellä olevan summa -ominaisuuden käyttöä ominaisuus on otettava käyttöön ja oletusasetukset määritettävä

1)  Valitse **Myyntireskontra > Parametrit > Täsmäytykset** tai **Ostoreskontra > Parametrit > Täsmäytykset**.
2)  Valitse ensin **Tilitys**-välilehti ja sitten **Ota jäljellä olevan summan selvitys käyttöön**.
3)  Valitse **Oletussyykoodi**-kohdassa oletussyykoodi. Syykoodi on oltava määritetty jo aiemmin kohdassa **Myyntireskontra > Asetukset > Asiakkaan poiskirjauksen syykoodit** tai **Ostoreskontra > Asetukset > Asiakkaan poiskirjauksen syykoodit**. **Jäljellä olevan summan selvityksen oletustili** on oletusarvoisesti tili, joka on määritetty poiskirjauksen syykoodille.
3)  Päivitä **Jäljellä olevan summan selvityksen oletustili** tarvittaessa.
4)  Valitse **Kirjauskansion oletusnimi** -kohdassa maksukirjauskansio, jota käytetään, jos haluat luoda maksukirjauskansion, kun tilität vain avoimia tapahtumia. Jos otat jäljellä olevan summan selvittämisominaisuuden käyttöön, oletuskirjauskansion nimi on lisättävä.

## <a name="settle-remainder-from-a-journal"></a>Jäljellä olevan summan selvittäminen kirjauskansiosta
Vaikka et ottaisi **Selvitä jäljellä olevan summa** -ominaisuutta käyttöön, voit silti kirjata tapahtuman kirjauskansiossa ja täsmäyttää sitten tapahtumat sen perusteella entiseen tapaan. Jos napsautat **OK**-painiketta, laskun avoimesta saldosta vähennetään käteissumma. Jos laskua ei voi kokonaan selvittää käteisellä, lasku jää avoimeksi ja jäljelle jäävä summa on selvitettävä myöhemmin.

Kun **Selvitä jäljellä olevan summa** -ominaisuus on otettu käyttää, voit selvittää jäljellä olevan summan kirjanpitotilille. Voit myös siirtää jäljellä olevan summan toiselle asiakastilille (asiakastapahtumat) tai toiselle toimittajalle (toimittajatapahtumat) sen sijaan, että laskut jäisivät avoimiksi. 

Selvitä jäljellä jäävä summa **Tilitys**-sivulla seuraavasti:

1)  Merkitse **Tilitys**-sivulla laskut tai tapahtumat, jotka haluat selvittää.
2)  Napsauta **Selvitä jäljellä oleva summa** -painiketta.
3)  Avautuvassa valintaikkunassa näkyy kirjanpitotilille selvitettävä summa ja päivämäärä, jolloin jäljellä oleva summa selvitetään, sekä parametreista saatu oletussyykoodi ja oletustili. 
4)  Valitse uusi tilityssyy, jos haluat vaihtaa oletussyyn. Tilitystiliksi vaihdetaan syykoodiin liitetty tili.
5)  Muokkaa tilitystiliä, jos haluat vaihtaa sen.
6)  Jos selvität asiakastapahtumia ja haluat, että jäljellä oleva summa siirretään toiselle asiakkaalle, valitse asiakas **Selvitä jäljellä oleva summa asiakastiliä vastaan** -kohdassa. Jos selvität toimittajatapahtumia ja haluat, että jäljellä oleva summa siirretään toiselle toimittajalle, valitse toimittaja **Selvitä jäljellä oleva summa toimittajatiliä vastaan** -kohdassa.
6)  Valitse **Selvitä jäljellä olevan summa**.
7)  **Kirjauskansio**-sivu avautuu. Kirjauskansioon lisätään kirjauskansion rivi, jossa summana on selvitettävä jäljellä oleva summa ja vastatilinä jäljellä olevan summan selvitystili. Jos olet lisännyt asiakkaan tai toimittajan siksi, että voi siirtää tilityssumman toiselle asiakkaalle tai toimittajalle, kirjauskansioon lisätään rivi, jolla tilityssumma siirretään kyseiselle asiakkaalle tai toimittajalle.

Kun kirjaat kirjauskansioon, avoin tapahtuma tilitetään kokonaan. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Jäljellä olevan summan selvittäminen vain avoimia tapahtumia selvitettäessä
Voit selvittää jäljelle olevan summan myös silloin, kun selvität avoimia tapahtumia ilman kirjauskansiota.

Jäljellä olevan summan voi selvittää seuraavasti:

1)  Merkitse **Tilitys**-sivulla laskut tai tapahtumat, jotka haluat selvittää.
2)  Valitse **Selvitä jäljellä olevan summa**.
3)  Avautuvassa valintaikkunassa näkyy kirjanpitotilille selvitettävä summa ja päivämäärä, jolloin jäljellä oleva summa selvitetään, sekä parametreista saatu oletussyykoodi ja oletustili. 
4)  Valitse uusi tilityssyy, jos haluat vaihtaa oletussyyn. Tilitystiliksi vaihdetaan syykoodiin liitetty tili.
5)  Muokkaa **tilitystiliä**, jos haluat vaihtaa sen.
6)  Jos selvität asiakastapahtumia ja haluat, että jäljellä oleva summa siirretään toiselle asiakkaalle, valitse asiakas **Selvitä jäljellä oleva summa asiakastiliä vastaan** -kohdassa. Jos selvität toimittajatapahtumia ja haluat, että jäljellä oleva summa siirretään toiselle toimittajalle, valitse toimittaja **Selvitä jäljellä oleva summa toimittajatiliä vastaan** -kohdassa.
7)  Voit luoda halutessasi myös maksukirjauskansion, jossa tilityksen jäljellä oleva summa on, tai vain kirjata sen ilman kirjauskansiota. Luo maksukirjauskansio valitsemalla **Kyllä** **Muokkaa kirjauskansiossa** -kohdassa Voi muokata luomaasi maksukirjauskansiota.
8)  Valitse **Selvitä jäljellä olevan summa**. Jos valitsit maksukirjauskansion luomisen, painikkeen tekstinä on **Luo kirjauskansio**. Valitse sen sijaan **Luo kirjauskansio**.
9)  Jos loit maksukirjauskansion, kirjauskansion sivu avautuu, kun valitsit **Selvitä jäljellä olevan summa**. Kirjauskansioon lisätään kirjauskansion rivi, jossa summana on selvitettävä jäljellä oleva summa ja vastatilinä jäljellä olevan summan selvitystili. Jos olet lisännyt asiakkaan tai toimittajan siksi, että voi siirtää tilityssumman toiselle asiakkaalle tai toimittajalle, kirjauskansioon lisätään rivi, jolla tilityssumma siirretään kyseiselle asiakkaalle tai toimittajalle.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]