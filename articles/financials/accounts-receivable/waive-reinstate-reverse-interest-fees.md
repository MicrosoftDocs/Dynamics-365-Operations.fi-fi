---
title: Luovu, palauta tai peruuta korot
description: "Tässä artikkelissa kerrotaan, miten korot ja maksut peruutetaan ja palautetaan sekä käytetään käänteistä veloitusta."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: ae4a84f0e2823d1e7686696eae72e050a320e3f1
ms.contentlocale: fi-fi
ms.lasthandoff: 02/07/2018

---

# <a name="waive-reinstate-or-reverse-interest-fees"></a>Luovu, palauta tai peruuta korot

[!include[banner](../includes/banner.md)]


Tässä artikkelissa kerrotaan, miten korot ja maksut peruutetaan ja palautetaan sekä käytetään käänteistä veloitusta.

Voit käyttää **Kaikki asiakkaat** -luettelosivun **Perintä** -välilehden painikkeita maksuista luopumiseen, peruuttamiseen tai palauttamiseen.

-   Peruutetut laskut annetaan anteeksi. Maksusta voidaan luopua, jos asiakas esimerkiksi riitauttaa veloituksen ja haluat säilyttää hyvät suhteet kyseisen asiakkaan kanssa.
-   Palautetut maksut erääntyvät uudelleen. Voit palauttaa aiemmin peruutetut maksut. Sinun on ehkä tarpeen palauttaa veloitus, jos tulet siihen tulokseen, että siitä ei olisi pitänyt luopua.
-   Peruutetut maksut poistetaan asiakkaan tililtä ja ne eivät enää eräänny. Voit peruuttaa maksut esimerkiksi silloin, kun asiakkaan velan laskemiseen valittiin väärä korkoprosentti. Voit käyttää erillistä prosessia koron uudelleenlaskemiseen ja luoda asiakkaalle korkolaskun uusilla veloituksilla.

Kaikki nämä toiminnot muuttavat korkolaskua. Korkolasku on liiketoiminta-asiakirja, joka ilmoittaa asiakkaille, kun korko tai maksut on veloitettu heidän tililleen. Kun luovut tai peruutat koron tai maksut, järjestelmä luo automaattisesti hyvityslaskun tai laskun oikaisun maksujen tilittämiseksi. Jos palautat peruutetut maksut, järjestelmä luo automaattisesti debet-summaisen laskun maksusta, jonka asiakas on velkaa. Seuraavassa taulukossa kuvataan kunkin toiminnon tulokset.

| Toiminto                                                                                                                                                                                                            | Tulos asiakkaalle                                                                                             | Prosessoi                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Luovu koko korkolaskusta kaikkien niiden sisältämien korkojen ja palkkioiden kanssa. –tai– Valitse ja luovu maksuista tai korkotapahtumista, jotka ovat osa korkolaskuja.                                        | Kulut annetaan anteeksi.                                                                                           | Asiakkaalle luodaan hyvityslasku tai laskun oikaisu. Asiakkaalle luodaan hyvityslasku tai oikaisulasku ja sitä käytetään automaattisesti korkolaskun tai valitsemiesi korkotapahtumien tai maksujen selvittämiseen. Selvitetty summa vastaa maksujen kokonaissummaa, joista on vähennetty asiakkaan suorittamat aiemmat maksut ja aiemmin luovutut tai pois kirjatut määrät. Jos hyvityslaskun summa ylittää asiakkaan velan määrän, voit muuttaa hyvityslaskun toimittajan laskuksi. Voit tämän jälkeen antaa asiakkaalle hyvityksen.                                                       |
| Palauta koko korkolasku kaikkien niiden sisältämien korkojen ja palkkioiden kanssa. –tai– Valitse ja palauta maksut tai korkotapahtumat, jotka ovat osa korkolaskuja.                                | Luovuttu määrä erääntyy uudelleen.                                                                                     | Järjestelmä luo laskun veloitussummalla ja summa tilitetään automaattisesti maksuihin, joista luovuttiin aiemmin. Todellisia korkolaskuja ei palauteta. Sen sijaan luodaan lasku, joka näyttää asiakkaalta erääntyvän summa. Hyvityslaskut tai oikaistut laskut, jotka luotiin peruutettujen korkolaskujen selvittämiseksi, voivat edelleen olla olemassa, jos niitä ei käytetty korkolaskujen selvittämiseen. Tässä tapauksessa avoimet hyvityslaskut peruutetaan. Avoimet hyvityslaskut tilitetään yleensä automaattisesti, kun korkolaskuista luovutaan. Avoin hyvityslasku voi kuitenkin olla olemassa, jos asiakas maksoi korkolaskun, vaikka asiakas riitautti maksut. |
| Palauta korkolaskut kokonaisuudessaan. –tai– Peruuta valitut korkotapahtumat, jotka ovat osa korkolaskuja. **Huomautus:** Et voi peruuttaa palkkiota. Voit kuitenkin peruuttaa koko korkolaskun, joka sisältää palkkion. | Maksut eivät enää eräänny asiakkaalta. Maksut erääntyvät kuitenkin uudelleen, jos korko lasketaan uudelleen. | Prosessi on sama kuin korkolaskuista tai valituista korkotapahtumista luopuminen. Asiakkaalle luodaan hyvityslasku tai laskun oikaisu. Tätä hyvityslaskua käytetään korkolaskun automaattiseen selvittämiseen. Voit käyttää erillistä prosessia koron uudelleenlaskemiseen ja uuden korkolaskun luontiin.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> Voit myös käyttää erillistä prosessia luottotappioiden poiskirjaukseen. Tämä prosessi merkitsee kaikki selvityksen asiakastapahtumat vain korkolaskujen osana olevien maksujen peruuttamisen sijaan.

## <a name="adjust-interest-for-invoices"></a>Lakujen korkojen oikaisu
Korkolaskujen oikaisujen lisäksi voit myös poistaa laskujen korkomaksut yhdellä seuraavista prosesseista. Molemmat prosessit suorittavat oikaisut myös liittyviin korkolaskuihin.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Korjaa lasku, jossa on liitetty korko

Voit korjata kirjatun laskun, joka sisältyy korkolaskuun. Tämä prosessi kopioi nykyisen laskun tiedot uuteen laskuun, jotta voit tehdä vain haluamasi korjaukset. Lasku peruutetaan ja järjestelmä luo uuden laskun. Myös tapahtuman korko palautetaan korkolaskuun, jos korkolasku kirjattiin. 

Voit tehdä korjaukset käyttämällä tekstimuotoisen laskun toimintoruudun **Korjaa lasku** -painiketta. Tämä painike on saatavilla vain, jos **Tekstimuotoisen laskun korjaus** -konfigurointiavain on valittuna.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Palauta asiakkaan tapahtuma, johon on liitetty korko

Voit palauttaa laskuun sisältyvän asiakastapahtuman, jos lasku on luotu virheellisesti. Jos palautettuun asiakastapahtumaan on sisällytetty korkolaskun korko ja korkolasku on kirjattu, myös korkolaskulla oleva tapahtuman korko palautetaan. Korkolasku peruutetaan, jos sitä ei ole kirjattu. 

Voit peruuttaa asiakastapahtumat käyttämällä **Peruuta**-painiketta **Asiakastapahtumat**-sivulla.

## <a name="waive-or-reinstate-interest-notes"></a>Korkolaskuista luopuminen tai niiden palauttaminen
Voit luopua valitsemiesi korkolaskujen kaikista maksuista tai palauttaa ne. Kun luovut maksuista, peruutettava kokonaissumma ei voi ylittää määritettyjä summien rajoja. Korkolaskun voi palauttaa vain, jos siitä on luovuttu aiemmin. 

Voit luopua korkolaskuista tai palauttaa ne käyttämällä **Korkolasku**-painiketta **Asiakas**-sivun **Perintä**-välilehdellä.

## <a name="waive-or-reinstate-interest-transactions"></a>Korkotapahtumista luopuminen tai niiden palauttaminen
Voit luopua tietyistä korkolaskun korkotapahtumista tai palauttaa ne korkolaskun kaikkien maksujen oikaisemisen sijaan. Kun luovut maksuista, peruutettava kokonaissumma ei voi ylittää määritettyjä summien rajoja. Korkotapahtuman voi palauttaa vain, jos siitä on luovuttu aiemmin. 

Voit luopua korkolaskusta tai palauttaa sen käyttämällä **Tapahtuman korko**-painiketta **Asiakas**-sivun **Perintä**-välilehdellä.

## <a name="waive-or-reinstate-fees"></a>Maksuista luopuminen tai niiden palauttaminen
Voit luopua tai palauttaa tietyt korkolaskun palkkiot korkolaskun kaikkien maksujen oikaisemisen sijaan. Kun luovut maksuista, peruutettava kokonaissumma ei voi ylittää määritettyjä summien rajoja. Voit palauttaa maksun ainoastaan, jos luovuit siitä aiemmin. 

Voit luopua korkolaskuista tai palauttaa ne käyttämällä **Maksu**-painiketta **Asiakas**-sivun **Perintä**-välilehdellä.

## <a name="reverse-interest-notes"></a>Palauta korkolaskut
Voit peruuttaa valitsemiesi korkolaskujen kaikki maksut. Peruutetut maksut poistetaan asiakkaan tililtä ja ne eivät enää eräänny. Kun korkolasku on peruutettu, voit laskea koron uudelleen ja luoda uuden korkolaskun. 

Voit peruuttaa korkolaskut käyttämällä **Korkolasku**-painiketta **Asiakas**-sivun **Perintä**-välilehdellä.

## <a name="reverse-interest-transactions"></a>Korkotapahtumien peruuttaminen
Voit peruuttaa kaikki valitsemasi korkotapahtumat. Peruutetut maksut poistetaan asiakkaan tililtä ja ne eivät enää eräänny. Kun tapahtumat on peruutettu, voit laskea koron uudelleen ja luoda uuden korkolaskun.

Voit peruuttaa korkotapahtumat käyttämällä **Tapahtuman korko** -painiketta **Asiakas**-sivun **Perintä**-välilehdellä.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>Tarkastele niiden maksujen oikaisujen historiatietoja, joista luovuttiin, jotka palautettiin tai peruutettiin
Voit tarkastella korkolaskuihin suoritettujen oikaisujen tarkkoja tietoja, kuten esimerkiksi oikaisun kirjoittanutta käyttäjää, oikaisun tyyppiä, määrää ja oikaisun kirjoituksen ajankohtaa. Saatat esimerkiksi ehkä haluta tarkastella korkolaskuun aiemmin tehtyjä muutoksia ennen uuden korkolaskun luomista. 

Voit peruuttaa korkotapahtumat käyttämällä **Historia**-painiketta **Asiakas**-sivun **Perintä**-välilehdellä.




