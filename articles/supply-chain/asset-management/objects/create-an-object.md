---
title: Luo resurssi
description: Tässä ohjeaiheessa kerrotaan, miten resurssi luodaan resurssien hallinnassa.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTableCopyStructure, EntAssetObjectTableCreate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28c4685c3b6f543324953cd03646d5b15fdb8c59
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019426"
---
# <a name="create-an-asset"></a>Luo resurssi

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan, miten resurssi luodaan resurssien hallinnassa.

1. Valitse **Resurssien hallinta** > **Yhteiset** > **resurssit** > **Kaikki resurssi** tai **Aktiiviset resurssit**.
2. Valitse **Uusi**-painike.
3. Lisää **Luo resursseja** -valintaikkunaan tiedot koskien **resurssia** (resurssin tunnus) ja resurssin nimeä. Valitse resurssille päivämäärä ja aika **Voimassa**-kentässä. Kyseisestä päivästä eteenpäin voit asentaa resurssin toiminnalliseen sijaintipaikkaan sekä siirtää ja korvata resurssin resurssirakenteessa.
4. Valitse **resurssityyppi** -kentässä resurssin tyyppi (pakollinen kenttä). Valitse tarvittaessa **resurssin valmistaja** ja **resurssin malli**. Jos vain yksi tuote on määritetty, kyseinen tuote valitaan automaattisesti **resurssin valmistaja** -kentässä. **Resurssin valmistaja**- ja **Resurssin malli** -kentissä käytettävissä olevat valinnat määräytyvät [resurssin valmistajien ja mallien](../setup-for-objects/product-and-model.md) asetusten mukaan.
5. **Ylätason resurssi** -ryhmässä **Resurssi**-kenttä on tyhjä oletusarvona. Voit tarvittaessa valita ylätason resurssin ja täyttää kaikki **Ylätason resurssi** -ryhmän kentät automaattisesti.
    >[!NOTE]  
    >Kun valitset ylätason resurssin, käytettävissä on kaksi tai kolme välilehteä: **Omat resurssit** -väliehti sisältää resurssit, jotka liittyvät toiminnallisiin sijainteihin, joihin sinut voidaan (järjestelmään kirjautuneena kunnossapitotyöntekijänä) kohdistaa. Jos [Ylläpitotyöntekijät ja työntekijäryhmät](../setup-for-objects/workers-and-worker-groups.md) -lomakkeessa ei ole määritetty toiminnallisia sijainteja ylläpitotyöntekijälle, **Omat resurssit** -välilehti ei ole näkyvissä. **Aktiiviset resurssit** -välilehti sisältää luettelon kaikista resursseista, joiden elinkaaritila on Aktiivinen. **Resurssinäkymä** -väli ehdessä näkyy puunäkymä toiminnallisista sijainneista ja näihin sijainteihin asennetuista resursseista.

6. Määritetty toiminnallinen oletussijainti on ehdotettu resurssille  **Resurssi**-ryhmän **Toiminnallinen sijainti** -kentässä. Valitse tarvittaessa toinen toiminnallinen sijainti.

    >[!NOTE]
    >Kun olet luonut resurssin, voit asentaa sen toiseen toimintosijaintiin tarvittaessa. Vain ylimmän tason resurssit (resurssit, joilla ei ole tällä hetkellä pääresurssia) voidaan asentaa toiminnallisessa sijainnissa. Tämä tarkoittaa, että asennat valittuun toimintosijaintiin ylimmän tason sekä mahdolliset aliresurssit. Lisätietoja resurssien asentamisesta toiminnallisiin sijainteihin on kohdassa [Toiminnallisten sijaintien esittely](../functional-locations/introduction-to-functional-locations.md).

7. Valitse **OK**.
8. Valitse resurssi **Kaikki resurssit** -luettelosta ja valitse **Muokkaa** -painike lisätäksesi lisätietoja resurssiin.

## <a name="general-information"></a>Yleistiedot

Funktionaalinen sijainti, johon käyttö omaisuuserä liittyy, näkyy **Toiminnallinen sijainti** -kentässä. Jos resurssi on pääresurssi, resurssiin liittyvien alitasojen määrä näkyy **Alitasot**-kentässä. Jos resurssi on luodun resurssin aliresurssi, pääresurssin tunnus määrä näkyy **Ylätaso**-kentässä.

Voit muokata **Resurssin valmistaja**- ja **resurssin malli** -kenttien tietoja resurssissa, jota käytetään varaosien, vaihtoehtoisten varaosien ja työtyypin oletusarvojen hallinnassa. Lisätietoja on kohdassa [Resurssin valmistajat ja mallit](../setup-for-objects/product-and-model.md). Voit myös tarvittaessa lisätä tietoja **Vuosimalli**- ja **Sarjanumero**-kenttiin.

**Nykyinen elinkaaren tila** -kenttää käytetään määritettäessä, onko resurssi aktiivinen vai passiivinen. Kun luot resurssin, vaiheeksi määritetään aina resurssin vaiheryhmän ensimmäinen vaihe. Kun olet valmis aktivoimaan resurssin, valitse **Päivitä resurssin tila** ja valitse se elinkaaren tila, jonka olet määrittänyt asetuksella "resurssi aktiivinen", ja valitse **OK**.

**Huomautus:** Kun resurssi on asetettu tilaan "passiivinen", ei ole enää mahdollista luoda työtilauksia resurssille. Et myöskään voi ajoittaa ennaltaehkäiseviä ylläpitotöitä passiiviselle resurssille.

**Palvelutaso** -ja **Kriittisyys**-kentät liittyvät resurssille luotuihin työtilauksiin. Kentissä näkyvät resurssin nykyisille asetuksille lasketut **Palvelutaso**- ja **Kriittisyys**-arvot. Lisätietoja näistä arvoista on kohdissa [Resurssin palvelutasot](../setup-for-objects/object-priorities.md) ja [Resurssin kriittisyystyypit](../setup-for-objects/object-criticalities.md).

## <a name="asset"></a>Resurssi

Voit valita resurssille kohteen **Resurssi**. Resurssin valinta määrittää, mitä kalenteria työtilausten ajoituksessa käytetään. Resurssien valintaa käytetään usein käyttöomaisuudelle. Resurssit ja resurssiryhmät määritetään valitsemalla **Organisaation hallinta** > **Resurssit** > **Resurssiryhmät** tai **Resurssit**.

**Käyttöomaisuuserän numero** -kentässä voidaan valita käyttöomaisuuserä, joka liittyy resurssiin. Tämä on merkityksellistä, jos resurssi liittyy investointiprojektiin.

- Jos resurssi liittyy käyttöomaisuuteen, voit luoda työtilauksen tyypin, jota käytetään investointiprojektiin liittyvissä työtilauksissa. 
- Resurssin käyttöomaisuutta koskevat tiedot liittyvät **Käyttöomaisuuserät**-moduuliin Dynamics 365 Supply Chain Managementissa. Tämä tarkoittaa sitä, että kohdassa **Käyttöomaisuuserät** >  **Käyttöomaisuuserät** >  **Käyttöomaisuuserät** voit saada yleiskatsauksen resurssien hallinnan projekteihin, jotka voivat liittyä käyttöomaisuuserään valitsemalla resurssin luettelosta ja tarkastelemalla sisältöä **Aiheeseen liittyvät tiedot**-ruudun **Liittyvät projektit** -osassa.


## <a name="details"></a>Yksityiskohdat

**Aktiivinen alkaen** -kentässä näkyy päivämäärä, jolloin resurssin elinkaaren tilaksi päivitettiin Aktiivinen (ks. [Resurssin elinkaaren tilat](../setup-for-objects/object-stages.md) koskien resurssien elinkaaren tilan määritystä). Jos resurssi ei ole enää aktiivinen ja olet päivittänyt resurssin elinkaaren tilaksi Passiivinen, päivä määrä, josta lähtien resurssi on passiivinen, näytetään **Aktiivinen saakka** -kentässä. Tarvittaessa voit muuttaa näitä päivämääriä manuaalisesti.

Voit tarvittaessa lisätä odotetun päivämäärän resurssin korvaamiseen **Korvauspäivämäärä**-kentässä. Resurssin korvaamista koskeva arvioitu arvo voidaan lisätä **Korvaava arvo** -kenttään. Esimerkki: Voit käyttää korvaustietoja, kun haluat verrata sitä resurssin ylläpitokustannuksiin, ja tehdä myöhemmin päätös uuden hyödykkeen hankkimisesta, jos nykyisen resurssin ylläpitokustannukset kasvavat nopeasti.

## <a name="notes"></a>Muistiinpanot

Voit lisätä resurssiin liittyviä muistiinpanoja **Huomautukset**-pikavälilehdessä. Napsauta **Lisää aikaleima** -painiketta ennen muistiinpanon kirjoittamista, jos haluat lisätä muistiinpanoon käyttäjätietoja ja päivämäärä-/aikaleiman.

## <a name="attributes"></a>Ominaisuudet

Tässä pikavälilehdessä voit määrittää resurssimääritteiden arvot. Näiden määritteiden avulla voidaan kuvata resurssin ominaisuuksia, esimerkiksi kokoa, painoa tai koneen kokoonpanoa.

Valitse **Lisää rivi** ja valitse määritetyyppi. Lisää seuraavaksi määritetyyppiin liittyvä **Arvo** ja tallenna tietue.

>[!NOTE] 
>Voit saada yleiskatsauksen resurssimääriteyypeistä ja niiden suhteesta resursseihin **Resurssimäärite** -ja **Resurssimääritteen yleiskatsaus** -kohdissa. Lisätietoja on kohdassa [Resurssimääritteen yleiskuvaus](../objects/object-specification-overview.md).

## <a name="vendor"></a>Toimittaja

Valitse **Toimittaja**-pikavälilehdessä resurssin toimittajan tili. Lisäksi, jos toimittajan takuu on myönnetty, voit lisätä takuutiedot tähän.

## <a name="address"></a>Osoite

**Osoite**-pikavälilehdessä voit lisätä laitteen osoitteen. Jos resurssiin ei ole lisätty osoitetta, resurssi käyttää pääresurssin osoitetta, jos pääresurssilla on osoite. Jos mitään osoitetta ei liity resurssihierarkiaan tai ylätasoihin, sen toiminnallisen sijainnin osoitetta, johon resurssi on asennettu, voidaan käyttää. Jos kyseisellä toiminnallisella paikalla ei ole siihen liittyvää osoitetta, resurssin ylätason toiminnallisen sijainnin osoitetta käytetään.

## <a name="asset-management-plans"></a>Resurssien hallinnan suunnitelmat

Huoltosuunnitelmia käytetään ennakoivan kunnossapidon töiden ajoittamiseen resurssille säännöllisin väliajoin. Tässä pikavälilehdessä voit määrittää valitun resurssin kunnossapitosuunnitelman rivit. Huoltokierroksia voidaan määrittää eri resursseille, joihin on suoritettava samanlainen tehtävä säännöllisin väliajoin. **Toiminnallisen sijainnin ylläpitosuunnitelmat** -välilehdellä näet kunnossapitosuunnitelmat, jotka liittyvät siihen toiminnalliseen sijaintiin, johon resurssi on asennettu.

>[!NOTE]
>Jos poistat resurssiiin liittyvän ylläpitosuunnitelman rivin tai ylläpitokierroksen **Kaikki resurssit** -kohdassa, poistat myös automaattisesti kaikki kunnossapitoaikataulut, joiden tila on Luotu ja jotka on luotu kyseisen ylläpitosuunnitelman tai ylläpitokierroksen perusteella.

## <a name="functional-location-maintenance-plans"></a>Toiminnallisten sijaintien ylläpitosuunnitelmat

Tällä pikavälilehdellä näet yleiskuvauksen kunnossapitosuunnitelmista, jotka liittyvät siihen toiminnalliseen sijaintiin, johon resurssi on asennettu.

## <a name="maintenance-rounds"></a>Ylläpitokierrokset

Tässä pikavälilehdessä voit lisätä tai poistaa ylläpitokierroksia, jotka liittyvät resurssiin.

## <a name="financial-dimensions"></a>Taloushallinnon dimensiot

Voit valita resurssille taloushallinnon dimensiot.
