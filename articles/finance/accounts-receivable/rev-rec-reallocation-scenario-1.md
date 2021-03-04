---
title: Tuottokirjauksen uudelleenkohdistus – skenaario 1
description: Tässä ohjeaiheessa käydään läpi uudelleenkohdistusskenaario, jossa kaksi myyntitilausta syötetään mutta ainoastaan vahvistetaan. Sama skenaario tuottaa samanlaisia tuloksia, jos enemmän kuin kaksi myyntitilausta on vahvistetussa tilassa.
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
ms.openlocfilehash: 2a0add2d4bc01127c1f359736398123a6a3df9fe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969649"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Tuottokirjauksen uudelleenkohdistus – skenaario 1

[!include [banner](../includes/banner.md)]

Tässä ohjeaiheessa käydään läpi uudelleenkohdistusskenaario, jossa kaksi myyntitilausta syötetään mutta ainoastaan vahvistetaan. Sama skenaario tuottaa samanlaisia tuloksia, jos enemmän kuin kaksi myyntitilausta on vahvistetussa tilassa.

Tätä skenaariota varten **Kirjaa laskun korjaukset myyntireskontraan** ‑asetukseksi on määritetty **Ei** **Kirjanpitoparametrit**-sivun **Tuottokirjaus**-välilehdessä (**Tuottokirjaus \> Asetukset \> Kirjanpitoparametrit**).

[![Kirjaa laskun korjaukset myyntireskontraan ‑asetuksena on Ei](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Asiakkaalle US\_SI\_0003 luodaan myyntitilaus. Asiakas ostaa kannettavan tietokoneen (nimiketunnus S0012) ja tukipalvelun sille (nimiketunnus S0008, ”Jatkuva tekninen palvelu”). Tuotto kannettavasta tietokoneesta kirjataan välittömästi (tuottokirjausaikataulua ei ole). Tukipalvelun tuottoa lykätään ja se kirjataan 12 kuukauden aikana sopimuksen päivämäärävälin määrittämällä tavalla.

[![Kannettavan tietokoneen ja tukipalvelun myyntitilausrivit](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Myyntitilaus vahvistetaan. Koska molemmille nimikkeille on määritetty tuottohinnan kohdistus, tuottohinta lasketaan, kun myyntitilaus vahvistetaan. Voit tarkastella kirjattavaa tuottoa **Tuottohinnan kohdistus** ‑sivulla (valitse **Myyntitilaus**-sivulla toimintoruudun **Hallinta**-välilehdessä **Tuottokirjaus**-ryhmässä **Tuottohinnan kohdistus**). Kannettavan tietokoneen tuotto kirjataan tuottotilille, ja summaksi tulee 1 008,01 $. Tukipalvelun tuotto kirjataan lykätyn tuoton tilille, ja summaksi tulee 190,99 $. Tuottohintojen summan on oltava sama kuin niiden tuottohinnan kohdistusta varten määritettyjen rivien summa (1 199,00 $).

[![Tuottohinnan kohdistus ‑sivu](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Asiakas päätti myyntihetkellä olla ostamatta asennuspalveluita (nimiketunnus S0001), mutta muutti myöhemmin mielensä. Tämän vuoksi samalle asiakkaalle syötetään toinen myyntitilaus.

[![Asennuspalveluiden myyntitilausrivi](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Toinen myyntitilaus vahvistetaan. Koska tämä myyntitilaus sisältää vain yhden rivin, tuottohinnan kohdistusta ei tehdä, kun myyntitilaus vahvistetaan. Tuottohinnan kohdistus tapahtuu vain, jos yksilöllisiä nimikkeitä on kaksi tai enemmän ja jos kyseisille nimikkeille on määritetty tuottohinnan kohdistus.

Jos tämä uusi myyntitilaus on ainoa muutos asiakkaan sopimukseen, uudelleenkohdistusprosessi voidaan nyt suorittaa. Avaa **Kohdista hinta uudelleen uusille tilausriveille** ‑sivu valitsemalla jommassakummassa myyntitilauksessa **Kohdista hinta uudelleen uusille tilausriveille**. Vaihtoehtoisesti voit valita **Tuottokirjaus \> Kausittaiset tehtävät \> Kohdista hinta uudelleen uusille tilausriveille**. Valitse kaksi myyntitilausta ja vastaavat myyntitilausrivit ja valitse sitten **Päivitä uudelleenkohdistus**. **Uudelleenkohdistettu summa** ‑sarakkeessa näkyy kunkin myyntitilausrivin uusi tuottohinta.

[![Uudet tuottohinnat Kohdista hinta uudelleen uusille tilausriveille ‑sivulla](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Jos valitset **Odotettu tosite**, mitään ei näytetä, koska laskuja ei ole kirjattu.

Viimeistele uudelleenkohdistus valitsemalla **Käsittele**. Sinua kehotetaan antamaan kirjauspäivämäärä, vaikka mitään ei olisi kirjattu. Kun uudelleenkohdistus on valmis, kunkin myyntitilauksen **Tuottohinnan kohdistus** ‑sivulla näkyy kaikkien nimikkeiden hinnan kohdistus molemmissa myyntitilauksissa. Toisin sanoen kunkin myyntitilauksen **Tuottohinnan kohdistus** ‑sivulla on nimike, jota ei ole myyntitilauksessa, koska se on osa samaa sopimusta mutta eri myyntitilauksessa.

> [!TIP]
> Jos haluat antaa kontekstitietoja siitä, miksi nämä lisänimikkeet näytetään, voit lisätä ruudukkoon muita sarakkeita, kuten **Uudelleenkohdistustunnus** ja **Myyntitilaus**.
> 
> [![Lisäsarakkeet Tuottohinnan kohdistus ‑sivulla](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)
