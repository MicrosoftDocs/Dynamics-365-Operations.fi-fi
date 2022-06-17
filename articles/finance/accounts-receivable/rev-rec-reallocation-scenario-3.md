---
title: Tuottokirjauksen uudelleenkohdistus – skenaario 3
description: Tässä artikkelissa käydään läpi uudelleenkohdistusskenaario, jossa aiemmin luotuun, laskutettuun myyntitilaukseen lisätään uusi rivi. Kun uusi nimike lisätään sopimukseen, sen voi lisätä uuteen myyntitilaukseen tai aiemmin luotuun myyntitilaukseen.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7aa62406a80eb3381206172caaae457ec71b7bf8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904813"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Tuottokirjauksen uudelleenkohdistus – skenaario 3

[!include [banner](../includes/banner.md)]

Tässä artikkelissa käydään läpi uudelleenkohdistusskenaario, jossa aiemmin luotuun, laskutettuun myyntitilaukseen lisätään uusi rivi. Kun uusi nimike lisätään sopimukseen, sen voi lisätä uuteen myyntitilaukseen tai aiemmin luotuun myyntitilaukseen. Tämä skenaario osoittaa myös, mitä tapahtuu, kun myyntireskontra päivitetään uudelleenkohdistusten vuoksi.

Tätä skenaariota varten **Kirjaa laskun korjaukset myyntireskontraan** ‑asetukseksi on määritetty **Kyllä** **Kirjanpitoparametrit**-sivun **Tuottokirjaus**-välilehdessä (**Tuottokirjaus \> Asetukset \> Kirjanpitoparametrit**).

[![Kirjaa laskun korjaukset myyntireskontraan ‑asetuksena on Kyllä.](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Asiakkaalle US\_SI\_0003 luodaan myyntitilaus. Asiakas ostaa kannettavan tietokoneen (nimiketunnus S0012) ja tukipalvelun sille (nimiketunnus S0008, ”Jatkuva tekninen palvelu”). Kannettavan tietokoneen tuotto kirjataan heti. Tukipalvelun tuottoa lykätään ja se kirjataan 12 kuukauden aikana sopimuksen päivämäärävälin määrittämällä tavalla.

[![Kannettavan tietokoneen ja tukipalvelun myyntitilausrivit.](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Myyntitilaus vahvistetaan. Koska molemmille nimikkeille on määritetty tuottohinnan kohdistus, tuottohinta lasketaan, kun myyntitilaus vahvistetaan. Voit tarkastella kirjattavaa tuottoa **Tuottohinnan kohdistus** ‑sivulla (valitse **Myyntitilaus**-sivulla toimintoruudun **Hallinta**-välilehdessä **Tuottokirjaus**-ryhmässä **Tuottohinnan kohdistus**). Kannettavan tietokoneen tuotto kirjataan tuottotilille, ja summaksi tulee 1 008,01 $. Tukipalvelun tuotto kirjataan lykätyn tuoton tilille, ja summaksi tulee 190,99 $. Tuottohintojen summan on oltava sama kuin niiden tuottohinnan kohdistusta varten määritettyjen rivien summa (1 199,00 $).

[![Tuottohinnan kohdistus ‑sivu.](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Myyntitilaus laskutetaan kokonaan. Seuraavassa kuvassa näkyy laskulle kirjattu kirjanpitomerkintä.

[![Kokonaan laskutetun myyntitilauksen kirjanpitomerkintä.](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Myös tuottokirjausaikataulu luodaan. Jonkin ajan kuluttua kahdella kuukaudella on kirjattua tuottoa tukipalvelusta.

[![Tuottokirjausaikataulu-sivu kahden kuukauden jälkeen.](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

Tässä vaiheessa asiakas päättää lisätä asennuspalvelut (nimiketunnus S0001). Tämä nimike lisätään aiemmin luotuun myyntitilaukseen. Asiakasta pyydetään vahvistamaan, että hän haluaa muokata täysin laskutettua myyntitilausta, ja hän valitsee **Kyllä**.

[![Myyntitilaus, kun asennuspalveluiden rivi on lisätty.](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Jos tämä uusi nimike on ainoa muutos asiakkaan sopimukseen, uudelleenkohdistusprosessi voidaan nyt suorittaa. Avaa **Kohdista hinta uudelleen uusille tilausriveille** ‑sivu valitsemalla myyntitilauksessa **Kohdista hinta uudelleen uusille tilausriveille**. Valitse kaikki tämän myyntitilauksen myyntitilausrivit ja valitse sitten **Päivitä uudelleenkohdistus**. **Uudelleenkohdistettu summa** ‑sarakkeessa näkyy kunkin myyntitilausrivin uusi tuottohinta.

[![Uudet tuottohinnat Kohdista hinta uudelleen uusille tilausriveille ‑sivulla.](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Valitse seuraavaksi **Odotettu tosite**, jotta voit tarkastella kirjanpitomerkintöjä. Koska **Kirjanpitoparametrit**-sivulla on määritetty **Kirjaa laskun korjaukset myyntireskontraan** ‑asetukseksi **Kyllä**, nämä kirjanpitomerkinnät kirjataan kirjanpitoon hyvitysasiakirjan kautta ja myyntireskontrassa luodaan uusi lasku.

[![Kirjanpitomerkinnät Odotettu tosite -sivulla.](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

**Odotettu tosite** ‑sivulla neljä viimeistä riviä peruuttavat alkuperäisen kirjanpitomerkinnän kirjatusta laskusta. Ensimmäiset viisi riviä ovat laskulle kirjattavat uudet kirjanpitomerkinnät. Huomaa, että asiakkaalle ei esitetä uutta laskua. Uudelleenkohdistuksen jälkeen asiakas on edelleen velkaa 1 276,94 $ eli summan, joka on kirjattava myyntireskontraan uudessa kirjanpitomerkinnässä. Vastakirjausvero ja tuotto tai lykätty tuotto ovat 995,83 $ + 188,69 $ + 77,94 $ = 1 262,46 $. Tuoton tai lykätyn tuoton summa on muuttunut uudelleenkohdistuksen vuoksi. Erotus –14,48 $ kirjataan osittaisen laskun tuoton selvitystilille. Tämä saldo tyhjennetään, kun lasku kirjataan myyntitilaukseen lisätylle uudelle nimikkeelle.

Viimeistele uudelleenkohdistus valitsemalla **Käsittele**. Kirjauspäivämäärä syötetään. Kun uudelleenkohdistus on suoritettu, **Tuottohinnan kohdistus** ‑sivulla näkyy kaikkien kolmen nimikkeen hinnan uudelleenkohdistus.

[![Kaikkien kolmen nimikkeen hinnan uudelleenkohdistus Tuottohinnan kohdistus ‑sivulla.](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Myös tuottokirjausaikataulu päivitettiin uuden tuoton kohdistushinnan perusteella. Avaa myyntitilauksesta **Tuottokirjausaikataulu**-sivu. Nimikkeellä S0008 oli aiemmin 13 riviä (nimikkeelle oli määritetty 12 kuukauden aikataulu). Nyt rivejä on 39: 13 alkuperäistä aikatauluriviä, 13 peruutusaikatauluriviä ja 13 riviä, jotka perustuvat uuteen tuottohintaan.

[![Nimikkeen S0008 päivitetty Tuottokirjausaikataulu-sivu, jolla on 39 riviä.](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Kun valitset **Tosite**, laskukirjauskansiossa näkyy alkuperäinen kirjanpitomerkintä. Voit tarkastella peruuttavaa merkintää ja uutta kirjanpitomerkintää myyntitilauksesta valitsemalla toimintoruudussa **Tuoton oikaisut** ja valitsemalla sitten **Tosite**.

Avaa seuraavaksi **Kaikki asiakkaat** -sivu (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**), valitse asiakas **US\_SI\_0003** ja valitse sitten **Tapahtumat**. **Asiakastapahtumat**-sivulla näkyy alkuperäinen lasku (000006), peruutusasiakirja (000006-1) ja uusi lasku (000006-2). Alkuperäinen lasku ja peruutusasiakirja selvitetään toisiaan vasten, ja saldoksi tulee 0 (nolla). Tarkastelemalla kunkin asiakirjan tositetta voit nähdä vaikutuksen kirjanpitoon.

[![Alkuperäinen lasku, peruutusasiakirja ja uusi lasku Asiakastapahtumat-sivulla.](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Myyntitilaus laskutetaan uudelleen lisätyn nimikkeen osalta. Asiakkaalle esitettävä kokonaislasku on summalle 300,00 $ + 19,50 $ (vero) = 319,50 $. Seuraavassa kuvassa näkyy kirjattu kirjanpitomerkintä.

[![Tositetapahtumat-sivu, jolla on kirjattu kirjanpitomerkintä.](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Koska tuoton ja myynnin summa on suurempi kuin 319,50 $, kirjataan erotus 14,48 $. Tämä summa tyhjentää saldon osittaisen laskun tuoton selvitystililtä. Kyseinen saldo päivitettiin uuteen kirjanpitomerkintään, joka kirjattiin uudelleenkohdistuksen jälkeen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
