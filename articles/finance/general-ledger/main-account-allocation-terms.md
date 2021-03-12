---
title: Kohdistusehdot
description: Tässä ohjeaiheessa on tietoja päätilin kohdistusehtojen käyttämisestä.
author: rachel-profitt
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount, AllocationTerms
audience: Application User
ms.reviewer: roschlom
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-06-15
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f529852f63c3dd12064c74403a12f6f3041691e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988667"
---
# <a name="allocation-terms"></a>Kohdistusehdot

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa on tietoja päätilin kohdistusehtojen käyttämisestä. Kohdistusehtoja käytetään jaettaessa summia useiden kirjanpitotiliyhdistelmien kesken. Niiden avulla varmistetaan, että kulut tai tuotot veloitetaan oikealta kohteelta kirjanpidossa.

Kukin päätilille luomasi kohdistusehto määrittää tositteen prosenttiosuuden, joka kohdistetaan yhden lähteen päätililtä ja taloushallinnon dimensioiden yhdistelmältä. Lisäksi määritetään kohteen päätili ja taloushallinnon dimensiot, joihin summa kohdistetaan. 

Kun määrität kohdistuksessa lähteen taloushallinnon dimension, voit määrittää, onko kukin dimensio yksilöity vai yksilöimätön. Yksilöity ilmaisee, että lähdetapahtuman taloushallinnon dimension on vastattava valittua dimensiota. Jos valitset Yksilöimätön-arvon, taloushallinnon dimension arvo voi vaikuttaa vastaavuuteen.

Jos määrität kohdekirjanpitotilin kohdistusehdolle, määritä myös päätili, jolle summa kohdistetaan. Voit käyttää samaa päätiliä, johon lähdetapahtuma on kirjattu, tai eri päätiliä. Jos käytät samaa päätiliä, tietueen tallentamisen yhteydessä näkyviin tulee varoitus. Päätilin määrittämisen lisäksi sinun on määritettävä myös kohdedimensiot. Voit määrittää jokaisen dimension kohdalla, säilytetäänkö taloushallinnon lähdedimension arvon vai muutetaanko sitä. Jos valitset ei, taloushallinnon dimensiolle on valittava uusi arvo. Jos valitset Kyllä, lisätietoja ei tarvitse määrittää. Järjestelmä ylläpitää alkuperäistä talousdimensiota kirjaamisen yhteydessä.

Päätiliin voi lisätä rajoittamattoman määrän kohdistusehtoja. Kohdistusehtojen kohdistusten prosenttiosuuden summan on kuitenkin oltava 100 tai alle. Voit luoda kohdistuksia niin, että summa on alle 100 prosenttia, jos alkuperäisen tositteen summan osa jää lähdetalousdimensioihin. Kohdistusehdot voidaan lisätä päätiliin yrityksen ohituksena. Jos käytössä on jaettu tilikartta, kohdistusehdot on määritettävä jokaiselle yritykselle. **Kohdistusehdot**-painikkeen käyttäminen edellyttää, että valitset ensin **Kohdistus**-valintaruudun Yrityksen ohitus -kohdassa.

## <a name="allocation-term-example"></a>Esimerkki kohdistusehdosta
Olet määrittänyt organisaatiollesi kustannuspaikan nimeltä YRITYS. Sen numero on 000. Kun laskut kirjataan käyttökuluiksi, ne koodataan tässä YRITYS-kustannuspaikassa. Yritys on määrittänyt säännön, jonka mukaan käyttökulut on kohdistettava prosenttiosuutena jokaiseen yksittäiseen kustannuspaikkaan. Osaston ja liiketoimintayksikön muut talousdimensiot säilyvät samoina.

Tässä esimerkissä luodaan uusi kohdistusehto käyttökulujen päätilille. Kullekin kustannuspaikalle luodaan yksi rivi ja kohdistettava prosenttiosuus. Kunkin rivin jokaisen lähdetalousdimension **Valintaehdot**-arvo on **Yksilöity** **kustannuspaikalle** ja arvoksi määritetään 000: YRITYS. Osastolle ja liiketoimintayksikölle **Valintaehdot**-arvo on **Yksilöimätön**.

**Kohdekirjanpitotili**-pikavälilehdessä päätili on sama käyttökulutili ja **Säilytä lähdetalousdimensiot** -kohdan arvoksi määritetään **Kyllä** **liiketoimintayksikölle** ja **osastolle**. **Säilytä lähdetalousdimensiot** -kohdan arvoksi määritetään **Ei** **kustannuspaikassa** ja valittu arvo on kutakin vastaavaa kustannuspaikkaa varten, johon olet tekemässä kohdistusta. Jos kohdistettavia kustannuspaikkoja on kolme, luodaan kolme kohdistusehtotietuetta. Ainoa ero kunkin kohdistusehdon välillä on kustannuspaikka, joka määritetään kohdekirjanpitotilillä.

## <a name="create-an-allocation-term-on-a-main-account"></a>Kohdistusehdon luominen päätilille

1. Siirry **siirtymisruudussa** kohtaan **Modulit > Yleinen kirjanpito > Tilikartat > Tilit > Päätilit**.
2. Etsi haluamasi tietue luettelosta ja valitse se.
3. Valitse **Yritysten ohitukset** -pikavälilehdessä **Lisää**.
4. Valitse **Yritys** ja valitse sitten **Lisää**.
5. Valitse **Kohdistus**-valintaruutu.
6. Valitse **Kohdistusehdot** .
7. Valitse **Muokkaa**, jos haluat muokata oletustietuetta, tai valitse **Uusi**, jos haluat lisätä tietueen.
8. Anna **Prosentti**-kenttään niiden tositetapahtumien prosenttiosuus, jotka haluat kohdistaa.
9. Valitse **Lähdetalousdimensio**-pikavälilehden **Valintaehdot**-kohdassa jokaiselle talousdimensiolle vaihtoehto.
    - Jos valitset **Yksilöity**, valitse talousdimension arvo oikealla olevasta avattavasta ruudusta.
    - Jos valitset **Yksilöimätön**, talousdimension lisätietoja ei tarvita.
10. Valitse **Kohdekirjanpitotili**-pikavälilehden **Kohdetili**-kentässä päätili, jonne haluat kohdistaa tositetapahtuman prosenttiosuuden.
11. Valitse kunkin talousdimension **Säilytä lähdetalousdimensiot** -kohdassa vaihtoehto.
    - Jos valitset **Ei**, valitse talousdimension arvo avattavasta ruudusta oikealla, jonne haluat tositetapahtuman kohdistettavan.
    - Jos valitset **Kyllä**, lisätietoja ei tarvita. Järjestelmä säilyttää alkuperäisen tositteen arvon kohdistusta kirjattaessa.
12. Toista vaiheet 7–11 jokaisen lisäkohdistuksen kohdalla. Kaikkien kohdistusten summa osoitetaan **Kokonaisprosenttiosuus**-kentässä. Tämä summa ei voi olla yli 100.
13. Sulkee kaikki sivut.

>[!NOTE] 
> Voit vaihtoehtoisesti käyttää **Kopioi**-painiketta, jos haluat monistaa valitun kohdistuksen.

Kun kohdistusehto luodaan päätilille, järjestelmä kirjaa automaattisesti uuden tositteen, kun kirjataan kohdistusehtojen lähdetalousdimensioita vastaava tosite.
