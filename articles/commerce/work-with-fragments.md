---
title: Katkelmien käyttäminen
description: Tässä artikkelissa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f911c5ee209cfcde5d2b2aef2c8f7343eb694cd3
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183286"
---
# <a name="work-with-fragments"></a>Katkelmien käyttäminen 

[!include [banner](includes/banner.md)]

Tässä artikkelissa kuvataan, miksi, milloin ja miten osia käytetään Microsoft Dynamics 365 Commerce -sovelluksessa.

Osat mahdollistavat koko sivustossa uudelleenkäytettävien moduulin määritysten keskitetyn muokkauskokemuksen. Esimerkiksi ylä- ja alatunnisteet sekä ilmoituspalkit määritetään usein osiksi, koska ne jaetaan useille sivuille. Voit ajatella osia pienoisverkkosivuina, jotka voidaan lisätä sivuston muihin sivuihin. Osilla on oma elinkaarensa. Toisin sanoen ne luodaan, päivitetään, niihin viitataan ja ne poistetaan yksittäisinä entiteetteinä muokkaustyökaluissa.

Kun osat on määritetty, niitä voidaan käyttää aina, kun moduuleja voi käyttää sivuston rakenteessa. Osiin voi viitata sivuilla, asetteluissa, malleissa ja muissa osissa.

> [!NOTE]
> Osat voivat olla sisäkkäisiä jopa seitsemän tason syvyyteen muissa osissa.

Jos haluat edistää esimerkiksi kausiluonteista tapahtumaa useilla sivuston sivuilla, voit käyttää osia. Uuden osan luontiprosessin ensimmäinen vaihe on valita sen moduulin tyyppi, jolla haluat aloittaa. Tässä esimerkissä voit muodostaa osan hero-moduulista.

> [!NOTE]
> Osia voi muodostaa mistä tahansa moduulityypistä.

Tämän jälkeen voit määrittää hero-osaan määritetyn kampanjasisällön. Voit myös lokalisoida sen tarpeen mukaan. Uutta erillistä hero-osaa voi tämän jälkeen kuluttaa esimääritettynä moduulina koko sivustossa. Voit helposti lisätä sen malleihin, tiettyihin sivuihin tai muihin osiin, joissa voi olla hero-moduuleita.

Kaikki paikat, joihin osa lisätään, ovat viittauksia luotuun, keskitettyyn hero-osaan. Jos julkaiset osan muutokset, ne vaikuttavat heti kaikissa sivuston paikoissa, joissa osaan viitataan. Tämän vuoksi osat ovat tehokas tapa käyttää uudelleen moduulin määrityksiä sivustossa ja hallita niitä keskitetysti. Tämä tehostettu käyttö ketteröittää toimintoja ja auttaa vähentämään sivuston hallintaan liittyviä kustannuksia.

Seuraavassa kuvassa näkyy, kuinka osia voi käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa.

![Kuvassa näkyy, kuinka osia voidaan käyttää jaettujen moduulin määritysten keskitetyssä muokkauksessa sähköisen kaupankäynnin sivustossa.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Osan luominen

Voit luoda uuden osan tai tallentaa olemassa olevan osan määrityksen osana.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Aiemmin luodun moduulin määrityksen tallentaminen osana

Voit muuntaa aiemmin määritetyn moduulin uudelleenkäytettäväksi osaksi seuraavasti Commercen sivustonmuodostimessa.

1. Avaa sivu tai malli, joka sisältää osaksi muunnettavan moduulin.
1. Valitse vasemmalla jäsennysruudussa aiemmin määritetty moduuli tai valitse se suoraan visuaalisessa sivunmuodostimessa.
1. Valitse kolme pistettä (**...**) moduulin nimen vieressä joko jäsennysruudusta tai valitun moduulin työkaluriviltä visuaalisessa sivunmuodostimessa. 
1. Valitse **Jaa osana**. 
1. Anna **Tallenna osana** -valintaikkunassa osan nimi.
1. Valitse **OK**, jos haluat tallentaa moduulin määrityksen osana, joka voidaan lisätä muille sivuille.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Luo uusi osa

Uusi osa luodaan Commercen sivustonmuodostimessa seuraavasti:

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.
1. Valitse **Uusi**. Avautuvassa **Uusi osa** -valintaikkunassa näkyy kaikki käytettävissä olevat moduulityypit. Osat voi luoda mistä tahansa moduulityypistä, kuten aiemmin jo mainittiin.
1. Valitse fragmentin moduulityyppi.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Kun valitset yleisen säilömoduulin tyypin, osan päivittäminen ja määrittäminen sujuu joustavasti myöhemmin.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Osien lisääminen sivulle tai niiden poistaminen tai muokkaaminen

Seuraavissa ohjeissa kuvataan, miten osia lisätään, poistetaan ja muokataan.

### <a name="add-a-fragment"></a>Osan lisääminen

Osa lisätään sivulle Commercen sivustonmuodostimessa seuraavasti:

1. Valitse vasemmassa jäsennysruudussa tai suoraan visuaalisessa sivunmuodostimessa säilö tai paikka, johon alimoduulit voidaan lisätä.
1. Valitse kolme pistettä (**...**) säilön tai paikan nimen vieressä.  Vaihtoehtoisesti voit valita plusmerkin (**+**), jos visuaalinen sivunmuodostin on käytössä.  
1. Valitse **Lisää osa**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Jos säilö tai paikka ei tue uusia alimoduuleja, **Lisää osa** -vaihtoehto ei ole käytettävissä.
    
1. Hae **Lisää osa** -valintaikkunassa lisättävä osa ja valitse se. Jos käytettävissä olevia osia ei ole näkyvissä, sinun on ehkä ensin luotava osa moduulityypistä, jota valittu säilö tai paikka tukee.
1. Valitse haluamasi fragmentti lisätäksesi sen sivullasi olevaan säilöön tai paikkaan.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> Moduulit, jotka sallitaan säilössä tai paikassa, määräytyvät sivun mallin tai moduulien omien määritysten mukaan.

### <a name="remove-a-fragment"></a>Osan poistaminen

Osa poistetaan Commercen sivustonmuodostimessa sivulla olevasta paikasta tai säilöstä seuraavasti:

1. Valitse vasemmanpuoleisessa jäsennysruudussa poistettavan osan nimen vieressä oleva kolmen pisteen painike (**...**) ja valitse sitten roskakorisymboli.  Vaihtoehtoisesti voit valita osan visuaalisessa sivunmuodostimessa ja valita roskakorisymbolin osan työkalurivillä.
1. Kun sinua pyydetään vahvistamaan osan poistaminen, valitse **OK**.

> [!NOTE]
> Kun poistat osan sivulta, poistat vain viittauksen kyseiseltä sivulta. **Et** poista osaa sivustosta. Jos haluat poistaa osia sivustosta, käytä osan tarkistusohjelman käyttöliittymää. Voit poistaa osia sivustosta vain, jos niihin ei tällä hetkellä viitata sivuissa, malleissa tai muissa osissa.

### <a name="edit-a-fragment"></a>Osan muokkaaminen

Jos haluat muokata osia, sinun on käytettävä osan muokkausohjelman käyttöliittymää. Tämä on suunniteltu rajoitus. Sen avulla voidaan varmistaa, että tekijät eivät sekoita tietyn sivun moduulien muokkausprosessia sellaisten osien muokkausprosessiin, joita voidaan jakaa useille sivuille.

Osaa muokataan Commercen sivustonmuodostimessa seuraavasti:

1. Valitse vasemmanpuoleisessa siirtymisruudussa **Osat**.
1. Valitse **Osat**-kohdassa muokattava osa.
1. Muokkaa osan moduulin ominaisuuksia ja rakennetta tarpeen mukaan. Prosessi muistuttaa moduulien muokkausprosessia, jossa moduuleja muokataan sivueditorinäkymässä.

Voit muokata osaa myös valitsemalla sen sivulla, mallissa tai pääosassa ja valitsemalla sitten **Muokkaa osaa** -kohdan oikeanpuoleisessa ominaisuusruudussa.

### <a name="rename-a-fragment"></a>Katkelman nimeäminen uudelleen

Olemassa oleva katkelma nimetään uudelleen sivustonmuodostimessa seuraavasti.

1. Valitse vasemmassa siirtymisruudussa **Katkelmat**.
1. Valitse sen katkelman nimi, jonka haluat nimetä uudelleen.
1. Aloita katkelman muokkaaminen valitsemalla **Muokkaa**. Huomaa, että katkelmaa ei voi muokata, jos joku muu on jo muokkaamassa katkelmaa.
1. Valitse katkelman nimen vieressä oleva kynäsymboli katkelman ominaisuusruudusta.
1. Muokkaa katkelman nimeä tarpeen mukaan.
1. Vahvista nimenmuutos valitsemalla valintamerkki.
1. Valitse **Viimeistele muokkaus**.

Voit nimetä katkelman myöhemmin uudelleen muokkaamalla sivua ja valitsemalla sitten kynäsymbolin ominaisuusruudussa katkelman nimen vierestä.

## <a name="additional-resources"></a>Lisäresurssit

[Mallit ja asettelut – yleiskatsaus](templates-layouts-overview.md)

[Mallien käyttö](work-with-templates.md)

[Esimääritettyjen asettelujen käyttö](work-with-layouts.md)

[Julkaisuryhmien kanssa työskenteleminen](publish-groups.md)

[Versiohistorian näyttäminen sivujen ja osien palauttamista varten](version-history-revert.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
