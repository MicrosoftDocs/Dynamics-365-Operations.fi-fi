---
title: Tuottokirjauksen uudelleenkohdistus – skenaario 4
description: Tässä ohjeaiheessa käydään läpi uudelleenkohdistusskenaario, jossa aiemmin luodusta, osittain laskutetusta myyntitilauksesta poistetaan rivi. Tämä skenaario tuottaa saman tuloksen riippumatta siitä, poistetaanko rivi myyntitilauksesta vai määritetäänkö sen tilaksi Peruutettu.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 50a2d0d2ca28d9b62713502700f2c4bd2e42751e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238301"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Tuottokirjauksen uudelleenkohdistus – skenaario 4

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käydään läpi uudelleenkohdistusskenaario, jossa aiemmin luodusta, osittain laskutetusta myyntitilauksesta poistetaan rivi. Tämä skenaario tuottaa saman tuloksen riippumatta siitä, poistetaanko rivi myyntitilauksesta vai määritetäänkö sen tilaksi Peruutettu.

Tätä skenaariota varten **Kirjaa laskun korjaukset myyntireskontraan** ‑asetukseksi on määritetty **Ei** **Kirjanpitoparametrit**-sivun **Tuottokirjaus**-välilehdessä (**Tuottokirjaus \> Asetukset \> Kirjanpitoparametrit**).

[![Kirjaa laskun korjaukset myyntireskontraan ‑asetuksena on Ei](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Asiakkaalle US\_SI\_0003 luodaan myyntitilaus. Asiakas ostaa kannettavan tietokoneen (nimiketunnus S0012), asennuspalvelut (nimiketunnus S0001) ja tukipalvelun kannettavalle tietokoneelle (nimiketunnus S0008, ”Jatkuva tekninen palvelu”). Kannettavan tietokoneen ja asennuspalveluiden tuotto kirjataan heti. Tukipalvelun tuottoa lykätään ja se kirjataan 12 kuukauden aikana sopimuksen päivämäärävälin määrittämällä tavalla.

[![Kannettavan tietokoneen, asennuspalveluiden ja tukipalvelun myyntitilausrivit](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Myyntitilaus vahvistetaan. Koska kaikille kolmelle nimikkeelle on määritetty tuottohinnan kohdistus, tuottohinta lasketaan, kun myyntitilaus vahvistetaan. Voit tarkastella kirjattavaa tuottoa **Tuottohinnan kohdistus** ‑sivulla (valitse **Myyntitilaus**-sivulla toimintoruudun **Hallinta**-välilehdessä **Tuottokirjaus**-ryhmässä **Tuottohinnan kohdistus**). Kannettavan tietokoneen tuotto kirjataan tuottotilille, ja summaksi tulee 995,84 $. Myös asennuspalveluiden tuotto kirjataan tuottotilille, ja summaksi tulee 314,47 $. Tukipalvelun tuotto kirjataan lykätyn tuoton tilille, ja summaksi tulee 188,69 $. Tuottohintojen summan on oltava sama kuin niiden tuottohinnan kohdistusta varten määritettyjen rivien summa (1 499,00 $).

[![Tuottohinnan kohdistus ‑sivu](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Asiakasta laskutetaan kannettavasta tietokoneesta ja tukipalvelusta, mutta ei asennuspalveluista. Seuraavassa kuvassa näkyy laskulle kirjattu kirjanpitomerkintä.

[![Laskutetun myyntitilauksen kirjanpitomerkintä](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Kirjanpitotapahtuma kirjaa 1 276,94 $ myyntireskontraan. Koska lasku on osalasku, tuoton tai lykätyn tuoton ja veron yhteenlaskettu summa ei kuitenkaan ole yhtä suuri kuin myyntireskontran summa. Erotus –14,47 $ kirjataan osittaisen laskun tuoton selvitystilille.

Myös tuottokirjausaikataulu luodaan.

[![Osalaskun Tuottokirjausaikataulu-sivu](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Asiakas päättää myöhemmin olla sittenkin ostamatta asennuspalveluita. Tämä rivi poistetaan siis myyntitilauksesta. Huomaa, että myyntitilausta ei voi vahvistaa uudelleen, koska vain laskutetut rivit säilyvät myyntitilauksessa.

[![Myyntitilaus, kun asennuspalveluiden rivi on poistettu](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Vaikka myyntitilausta ei voi vahvistaa, sen voi kohdistaa uudelleen. Avaa **Kohdista hinta uudelleen uusille tilausriveille** ‑sivu valitsemalla myyntitilauksessa **Kohdista hinta uudelleen uusille tilausriveille**. Valitse kaksi jäljellä olevaa myyntitilausriviä ja valitse sitten **Päivitä uudelleenkohdistus**. **Uudelleenkohdistettu summa** ‑sarakkeessa näkyy kunkin jäljellä olevan myyntitilausrivin uusi tuottohinta.

[![Uudet tuottohinnat Kohdista hinta uudelleen uusille tilausriveille ‑sivulla](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Valitse seuraavaksi **Odotettu tosite**, jotta voit tarkastella kirjanpitomerkintöjä.

[![Kirjanpitomerkinnät Odotettu tosite -sivulla](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

**Odotettu tosite** ‑sivulla viisi viimeistä riviä peruuttavat alkuperäisen kirjanpitomerkinnän kirjatusta laskusta. Ensimmäiset neljä riviä ovat laskulle kirjattavat uudet kirjanpitomerkinnät. Huomaa, että asiakkaalle ei esitetä uutta laskua. Uudelleenkohdistuksen jälkeen asiakas on edelleen velkaa 1 276,94 $ eli summan, joka on kirjattava myyntireskontraan uudessa kirjanpitomerkinnässä. Uusi tuotto tai lykätty tuotto sekä vero ovat yhteensä 1 276,94 $. Näin ollen sinun ei tarvitse tehdä kirjausta osittaisen laskun tuoton selvitystilille.

Viimeistele uudelleenkohdistus valitsemalla **Käsittele**. Kirjauspäivämäärä syötetään. Kun uudelleenkohdistus on suoritettu, **Tuottohinnan kohdistus** ‑sivulla näkyy kahden jäljellä olevan nimikkeen hinnan uudelleenkohdistus.

[![Jäljellä olevien nimikkeiden hinnan uudelleenkohdistus Tuottohinnan kohdistus ‑sivulla](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Myös tuottokirjausaikataulu päivitettiin uuden tuoton kohdistushinnan perusteella. Avaa myyntitilauksesta **Tuottokirjausaikataulu**-sivu. Nimikkeellä S0008 oli aiemmin 13 riviä (nimikkeelle oli määritetty 12 kuukauden aikataulu). Nyt rivejä on 39: 13 alkuperäistä aikatauluriviä, 13 peruutusaikatauluriviä ja 13 riviä, jotka perustuvat uuteen tuottohintaan.

[![Nimikkeen S0008 päivitetty Tuottokirjausaikataulu-sivu, jolla on 39 riviä](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Kun valitset **Tosite**, laskukirjauskansiossa näkyy alkuperäinen kirjanpitomerkintä. Voit tarkastella peruuttavaa merkintää ja uutta kirjanpitomerkintää myyntitilauksesta valitsemalla toimintoruudussa **Tuoton oikaisut** ja valitsemalla sitten **Tosite**.

Avaa seuraavaksi **Kaikki asiakkaat** -sivu (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**), valitse asiakas **US\_SI\_0003** ja valitse sitten **Tapahtumat**. **Asiakastapahtumat**-sivulla näkyy vain alkuperäinen lasku (000008) yhdessä alkuperäisen kirjanpitomerkinnän kanssa. Koska **Kirjanpitoparametrit**-sivulla on määritetty **Kirjaa laskun korjaukset myyntireskontraan** ‑asetukseksi **Ei**, vain kirjanpito päivitetään. Tämän vuoksi peruuttavat ja päivitetyt kirjanpitomerkinnät eivät näy. Huomaa, että [skenaariossa 3](rev-rec-reallocation-scenario-3.md) luodut tuoton oikaisutapahtumat näytetään.

[![Alkuperäinen kirjanpitomerkintä Asiakastapahtumat-sivulla](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]