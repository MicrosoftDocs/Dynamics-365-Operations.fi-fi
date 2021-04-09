---
title: Tuottokirjauksen uudelleenkohdistus – skenaario 2
description: Tässä ohjeaiheessa käydään läpi uudelleenkohdistusskenaario, jossa syötetään kaksi myyntitilausta ja sitten asiakas lisää nimikkeen sopimukseen ensimmäisen myyntitilauksen laskuttamisen jälkeen. Kun uusi nimike lisätään sopimukseen, sen voi lisätä uuteen myyntitilaukseen tai aiemmin luotuun myyntitilaukseen.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 31a0b26fbf2383c90caaa8c1ea0e56ab5f377609
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814197"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Tuottokirjauksen uudelleenkohdistus – skenaario 2

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käydään läpi uudelleenkohdistusskenaario, jossa syötetään kaksi myyntitilausta ja sitten asiakas lisää nimikkeen sopimukseen ensimmäisen myyntitilauksen laskuttamisen jälkeen. Kun uusi nimike lisätään sopimukseen, sen voi lisätä uuteen myyntitilaukseen tai aiemmin luotuun myyntitilaukseen.

Tätä skenaariota varten **Kirjaa laskun korjaukset myyntireskontraan** ‑asetukseksi on määritetty **Ei** **Kirjanpitoparametrit**-sivun **Tuottokirjaus**-välilehdessä (**Tuottokirjaus \> Asetukset \> Kirjanpitoparametrit**).

[![Kirjaa laskun korjaukset myyntireskontraan ‑asetuksena on Ei](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Asiakkaalle US\_SI\_0003 luodaan myyntitilaus. Asiakas ostaa kannettavalle tietokoneelle asennuspalvelut (nimiketunnus S0001) ja tukipalvelun (nimiketunnus S0008) mutta ei ole vielä valinnut kannettavaa tietokonetta. Asennuspalveluiden tuottoa lykätään siihen päivämäärään asti, jolloin kannettava tietokone ostetaan. Tukipalvelun tuottoa lykätään ja se kirjataan 12 kuukauden aikana sopimuksen päivämäärävälin määrittämällä tavalla.

[![Asennuspalveluiden ja tukipalvelun myyntitilausrivit](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Myyntitilaus vahvistetaan. Koska molemmille nimikkeille on määritetty tuottohinnan kohdistus, tuottohinta lasketaan, kun myyntitilaus vahvistetaan. Voit tarkastella kirjattavaa tuottoa **Tuottohinnan kohdistus** ‑sivulla (valitse **Myyntitilaus**-sivulla toimintoruudun **Hallinta**-välilehdessä **Tuottokirjaus**-ryhmässä **Tuottohinnan kohdistus**). Asennuspalveluiden tuotto kirjataan lykätyn tuoton tilille, ja summaksi tulee 250,00 $. Myös tukipalvelun tuotto kirjataan lykätyn tuoton tilille, ja summaksi tulee 150,00 $. Tuottohintojen summan on oltava sama kuin niiden tuottohinnan kohdistusta varten määritettyjen rivien summa (400,00 $).

[![Tuottohinnan kohdistus ‑sivu](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Myyntitilaus laskutetaan kokonaan. Seuraavassa kuvassa näkyy laskulle kirjattu kirjanpitomerkintä.

[![Kokonaan laskutetun myyntitilauksen kirjanpitomerkintä](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Lisäksi luodaan tuottokirjausaikataulu, mutta mitään tuottoa ei vielä kirjata.

[![Tuottokirjausaikataulu-sivu](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

Muutamaa päivää myöhemmin asiakas valitsee kannettavan tietokoneen. Asiakkaalle syötetään toinen myyntitilaus.

[![Kannettavan tietokoneen myyntitilausrivi](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Toinen myyntitilaus vahvistetaan. Koska tämä myyntitilaus sisältää vain yhden rivin, tuottohinnan kohdistusta ei tehdä, kun myyntitilaus vahvistetaan. Tuottohinnan kohdistus tapahtuu vain, jos yksilöllisiä nimikkeitä on kaksi tai enemmän ja jos kyseisille nimikkeille on määritetty tuottohinnan kohdistus.

Jos tämä uusi myyntitilaus on ainoa muutos asiakkaan sopimukseen, uudelleenkohdistusprosessi voidaan nyt suorittaa. Avaa **Kohdista hinta uudelleen uusille tilausriveille** ‑sivu valitsemalla jommassakummassa myyntitilauksessa **Kohdista hinta uudelleen uusille tilausriveille**. Vaihtoehtoisesti voit valita **Tuottokirjaus \> Kausittaiset tehtävät \> Kohdista hinta uudelleen uusille tilausriveille**. Valitse kaksi myyntitilausta ja vastaavat myyntitilausrivit ja valitse sitten **Päivitä uudelleenkohdistus**. **Uudelleenkohdistettu summa** ‑sarakkeessa näkyy kunkin myyntitilausrivin uusi tuottohinta.

[![Uudet tuottohinnat Kohdista hinta uudelleen uusille tilausriveille ‑sivulla](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Valitse seuraavaksi **Odotettu tosite**, jos haluat tarkastella vain kirjanpitoon kirjattavia kirjanpitomerkintöjä. Koska **Kirjanpitoparametrit**-sivulla on **Kirjaa laskun korjaukset myyntireskontraan** ‑asetuksena **Ei**, myyntireskontraan ei tehdä muutoksia, kun uudelleenkohdistus käsitellään.

[![Kirjanpitomerkinnät Odotettu tosite -sivulla](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

**Odotettu tosite** ‑sivulla kolme viimeistä riviä peruuttavat alkuperäisen kirjanpitomerkinnän kirjatusta laskusta. Ensimmäiset neljä riviä muodostavat laskulle kirjattavan uuden kirjanpitomerkinnän. Huomaa, että asiakkaalle ei esitetä uutta laskua. Uudelleenkohdistuksen jälkeen asiakas on edelleen velkaa 426,00 $ eli summan, joka on kirjattava myyntireskontraan uudessa kirjanpitomerkinnässä. Vastakirjausvero ja lykätty tuotto ovat 188,69 $ + 314,48 $ + 26,00 $ = 529,17 $. Lykätty tuottosumma on muuttunut uudelleenkohdistuksen vuoksi. Erotus 103,17 $ kirjataan osittaisen laskun tuoton selvitystilille. Tämä saldo tyhjennetään, kun lasku kirjataan toiselle uudelleenkohdistukseen sisältyvälle myyntitilaukselle.

Viimeistele uudelleenkohdistus valitsemalla **Käsittele**. Sinua kehotetaan antamaan kirjauspäivämäärä, vaikka mitään ei olisi kirjattu. Kun uudelleenkohdistus on valmis, kunkin myyntitilauksen **Tuottohinnan kohdistus** ‑sivulla näkyy kaikkien nimikkeiden hinnan kohdistus molemmissa myyntitilauksissa. Toisin sanoen kunkin myyntitilauksen **Tuottohinnan kohdistus** ‑sivulla on nimike, jota ei ole myyntitilauksessa, koska se on osa samaa sopimusta mutta eri myyntitilauksessa.

> [!TIP]
> Jos haluat antaa kontekstitietoja siitä, miksi nämä lisänimikkeet näytetään, voit lisätä ruudukkoon muita sarakkeita, kuten **Uudelleenkohdistustunnus** ja **Myyntitilaus**.
> 
> [![Lisäsarakkeet Tuottohinnan kohdistus ‑sivulla](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

Myyntitilauksessa 00036 päivitettiin myös tuottokirjausaikataulu uuden tuoton kohdistushinnan perusteella. Avaa tästä myyntitilauksesta **Tuottokirjausaikataulu**-sivu. Nimikkeellä S0008 oli aiemmin 13 riviä (nimikkeelle oli määritetty 12 kuukauden aikataulu). Nyt rivejä on 39: 13 alkuperäistä aikatauluriviä, 13 peruutusaikatauluriviä ja 13 riviä, jotka perustuvat uuteen tuottohintaan.

[![Nimikkeen S0008 päivitetty Tuottokirjausaikataulu-sivu, jolla on 39 riviä](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Vastaavasti nimikkeellä S0001 oli aiemmin kaksi riviä, mutta nyt niitä on kuusi.

[![Nimikkeen S0001 päivitetty Tuottokirjausaikataulu-sivu, jolla on kuusi riviä](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Kun valitset myyntitilauslaskussa 000036 **Tosite**, laskukirjauskansiossa näkyy alkuperäinen kirjanpitomerkintä. Voit tarkastella peruuttavaa merkintää ja uutta kirjanpitomerkintää myyntitilauksesta valitsemalla toimintoruudussa **Tuoton oikaisut** ja valitsemalla sitten **Tosite**.

[![Myyntitilaus 000036](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Avaa seuraavaksi **Kaikki asiakkaat** -sivu (**Myyntireskontra \> Asiakkaat \> Kaikki asiakkaat**), valitse asiakas **US\_SI\_0003** ja valitse sitten **Tapahtumat**. Näkyviin tulee myyntitilausrivin 000036 avoin lasku. Jos valitset tositteen, näet alkuperäisen kirjanpitomerkinnän, etkä uutta kirjanpitomerkintää uudelleenkohdistuksesta. Peruuttavaa merkintää ja uutta kirjanpitomerkintää ei voi tarkastella myyntireskontrasta.

Toinen myyntitilaus laskutetaan nyt. Asiakkaalle esitettävä kokonaislasku on summalle 1 099,00 $ + 71,44 $ (vero) = 1 170,44 $. Seuraavassa kuvassa näkyy kirjattu kirjanpitomerkintä.

[![Tositetapahtumat-sivu, jolla on kirjattu kirjanpitomerkintä](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Koska tuoton ja myynnin summa on suurempi kuin 1 170,44 $, kirjataan erotus –130,17 $. Tämä summa tyhjentää saldon osittaisen laskun tuoton selvitystililtä. Kyseinen saldo kirjataan uuteen kirjanpitomerkintään uudelleenkohdistuksen jälkeen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]