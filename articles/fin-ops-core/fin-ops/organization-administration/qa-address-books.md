---
title: Osoitekirjat – usein kysytyt kysymykset
description: Tässä ohjeaiheessa on vastauksia osoitekirjoihin liittyviin usein kysyttyihin kysymyksiin.
author: msftbrking
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyCheckDuplicate, DirPartyTable
audience: Application User
ms.reviewer: sericks
ms.custom: 23601
ms.assetid: b177fa0f-ac9a-415e-9498-15438e132f60
ms.search.region: Global
ms.author: brking
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 60e6fb7d38bd3ca78538ca10a15f6fb09bba52a3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693901"
---
# <a name="address-books-faq"></a>Osoitekirjat – usein kysytyt kysymykset

[!include [banner](../includes/banner.md)]

## <a name="how-do-i-check-for-duplicate-records"></a>Miten tietueiden kaksoiskappaleita etsitään?

Voit etsiä tietueiden kaksoiskappaleita suoraan **Yleisen osoitekirja** -luettelosivulta. Valitse toimintoruudun **Osapuoli**-välilehden **Ylläpidä**-ryhmässä **Tee kaksoisarvotarkistus**. Valitse sitten kaksoisarvotarkistukseen sisältyvät arvot.

## <a name="can-i-bulk-add-or-delete-party-records-from-an-address-book"></a>Voiko osoitekirjaan lisätä tai siitä poistetaan osapuolitietueita joukkona?

Kyllä. Voit lisätä useita osapuolitietueita osoitekirjaa ja myös poistaa niitä.

- Voit lisätä useita osapuolitietueiden osoitekirjaan valitsemalla **Yleinen osoitekirja** -luettelosivulla luettelosta osapuolet. Valitse sitten toimintoruudun **Osapuoli**-välilehden **Ylläpidä**-ryhmässä **Määritä osapuolet**. Valitse osoitekirjat, joihin haluat lisätä valitun osapuolitietueet, ja valitse sitten **OK**. Kaikki valitut osapuolitietueet lisätään kaikkiin valittuihin osoitekirjoihin.
- Voit poistaa useita osapuolitietueiden osoitekirjasta valitsemalla **Yleinen osoitekirja** -luettelosivulla luettelosta osapuolet. Valitse sitten toimintoruudun **Osapuoli**-välilehden **Ylläpidä**-ryhmässä **Poista osapuolet**. Valitse osoitekirjat, joista osapuolet poistetaan ja valitse sitten **OK**. Kaikki valitut osapuolitietueet poistetaan kaikista valituista osoitekirjoista.

## <a name="can-i-change-the-party-type-of-a-record-or-do-i-have-to-delete-the-old-record-and-create-a-new-one"></a>Voiko tietueen osapuolityyppiä muuttaa vai onko vanha tietue poistettava ja uusi luotava?

Aina silloin tällöin tietueen osapuolityyppi on vaihdettava henkilöstä organisaatioksi tai organisaatiosta henkilöksi. Esimerkiksi Nancy on Fabrikam UK:n myyntiryhmän jäsen. Hän tapaa Lontoossa messuilla kuusi uutta prospektia. Nancy luo kullekin prospektille prospektin osapuolitietueen. Kun Nancy tallentaa tietueet, jokainen tietue luodaan myös yleiseen osoitekirjaan. Fabrikam on määrittänyt organisaaton osapuolen oletustyypiksi, mutta kahden uuden prospektin tietueen tyyppinä pitäisi olla henkilö. Kun Nancy palaa messuilta, hänen onkin vaihdettava kahden prospektitietueen osapuolityyppi. Jotta osapuolitietueen tyypin voisi vaihtaa toiseksi tyypiksi, yleiseen osoitekirjaan on luotava ensin oikeantyyppinen uusi osapuolitietue. Voit sitten liittää vanhan osapuolitietueen tähän uuteen tietueen. Kun on tehnyt uuden osapuoliliitoksen, poista alkuperäinen osapuolitietue, jossa on virheellinen tietuetyyppi.

## <a name="how-do-i-change-the-name-or-address-of-a-party-record"></a>Miten osapuolitietueen nimi tai osoite voidaan muuttaa?

Voit koska tahansa päivittää osapuolitietueen nimet ja tietueeseen liitetyt osoitteet.

- Voit päivittää osapuolitietueen nimen avaamalla osapuolitietueen ja valitsemalla sitten toimintoruudussa **Muokkaa**. Anna **Yleinen**.pikavälilehdessä osapuolen uusi nimi ja tallenna sitten tietue.
- Voit päivittää osapuolitietueen osoitteen avaamalla osapuolitietueen ja valitsemalla sitten **Osoitteet**-pikavälilehdessä päivitettävä osoite. Valitse ensin **Muokkaa** ja tee sitten **Muokkaa osoitetta** -sivulla tarvittavat muutokset osoitteeseen tai osoiteparametreihin.

## <a name="can-i-merge-two-or-more-party-records-into-one-record"></a>Voiko kaksi tai sitä useampi osapuolitietue yhdistää yhdeksi tietueeksi?

Aina silloin tällöin voi olla tarpeellista yhdistää kaksi tai sitä useampi osapuolitietue yhdeksi tietueeksi. Niin on tehtävä esimerkiksi silloin jos luot vähintään yhdelle osapuolitietueelle kaksoiskappaleen joko tarkoituksella tai vahingossa. Osapuolitietueita yhdistettäessä yksi tietue valitaan säilytettäväksi. Muiden tietueiden tiedot yhdistetään sitten tähän tietueeseen. Jos esimerkiksi havaitset, että Fabrikamia koskevia tietoja on tallennettu kolmeen osapuolitietueeseen: A, B, and C. Päätät säilyttää osapuolitietueen A. Niinpä osapuolitietueissa B ja C tallennetut tiedot yhdistetään osapuolitietueeseen A. Tietyissä tilanteissa osapuolitietueita ei kuitenkaan voi yhdistää:

- Samaan osapuolirooliin, kuten asiakkaaseen tai toimittajaan, samassa yrityksessä liitettyjä osapuolitietueita ei voi yhdistää. Esimerkiksi osapuoli A on liitetty asiakkaaseen yrityksessä 123 ja osapuoli B on liitetty toiseen yrityksen 123 asiakkaaseen. Näitä osapuolitietueita ei voi yhdistää, koska jos ne yhdistettäisiin, yhdistetty osapuolitietue liitettäisiin useisiin asiakkaisiin samalla yrityksissä, mikä ei ole sallittua. Tietueet voidaan kuitenkin yhdistää, jos osapuoli B on liitetty toimittajaan yrityksessä 123 tai eri yrityksen asiakkaaseen.
- Saman yrityksen, ryhmän tai toimintayksikön sisäisen osapuoliorganisaation tietueita ei voi yhdistää.

## <a name="should-i-create-a-party-record-in-the-global-address-book-or-in-another-place-such-as-the-customer-or-vendor-page"></a>Pitäisikö osapuolitietue luoda yleisessä osoitekirjassa tai jossain muualla, kuten asiakas- tai toimittajasivulla?

Voit määrittää osapuolitietueet joko yleisessä osoitekirjassa tai soveltuvalla yksikkösivulla. Kun lisäät tietuen yhdessä sijainnissa, sama tietue lisätään aina myös toisessa sijainnissa. Jos esimerkiksi lisäät asiakkaan osapuolitietueen yleisessä osoitekirjassa, tietue lisätään myös **Asiakas**-sivulla. Samoin jos lisäät asiakkaan osapuolitietueen **Asiakas**-sivulla, tietue lisätään myös yleisessä osoitekirjassa. Päätä seuraavien ohjeiden avulla, missä uudet osapuolitietueet lisätään:

- **Osapuolitietueen luominen, kun yksikkötyyppi ei ole tiedossa** – Jos osapuolitietue on luotava, mutta yksikkötyyppi ei ole tiedossa. (Et esimerkiksi tiedä, onko yksikkö asiakas vai mahdollisuus). Voit valita yksikkötyypin myöhemmin.
- **Osapuolitietueen luominen, kun yksikkötyyppi on tiedossa** – Jos osapuolen yksikkötyyppi on tiedossa, voit luoda tietueen kyseisen tietueen sivulla. Voit esimerkiksi luoda asiakkaan tietueen **Asiakas**-sivulla. Kun luot ja tallennat tietueet soveltuvalla yksikkösivulla, tietue luodaan automaattisesti yleisessä osoitekirjassa.

## <a name="can-i-translate-address-information-for-party-records"></a>Voiko osapuolitietueiden osoitetiedot kääntää?

Voit määrittää osoitetietojen käännökset, jotta tiedot näkyvät käyttäjän kielellä (järjestelmän kieli) ohjelmassasi, mutta toisella kielellä asiakirjoissa, kuten myyntitilauksissa. Voit antaa maiden tai alueiden nimien, osoitekohteiden ja nimijaksojen käännökset. Jos järjestelmän kieli on esimerkiksi tanska, voit luoda myyntitilauksen ranskalaiselle asiakkaalle. Tässä tapauksessa voit tarkastella ongelmassa tanskankielistä asiakastietuetta, mutta osoitetiedot näkyvät tulostetussa myyntitilauksessa ranskaksi. Anna käännöksiä määritettäessä käännös luettelon jokaiselle nimikkeelle. Nimikkeet, joille ei annetta käännöstä, näkyvät järjestelmän kielellä. Jos järjestelmän kieli on esimerkiksi tanska, voit lähettää asiakirjan espanjalaiselle asiakkaalle. Jos et ole antanut osoitetietojen espanjankielisiä (ESP) käännöksiä, kyseiset tiedot näkyvät tanskaksi sekä ohjelmassa että tulostetussa asiakirjassa.
