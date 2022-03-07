---
title: Puhelinkeskuskanavan määrittäminen
description: Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.
author: samjarawan
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3b21d5e57058fee5bb77beb6731c18967ed11cacc1925e44d2f7d8cdb26d7bcb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744531"
---
# <a name="set-up-a-call-center-channel"></a>Puhelinkeskuskanavan määrittäminen


[!include [banner](includes/banner.md)]

Tässä ohjeaiheessa käsitellään uuden puhelinkeskuskanavan luontia Microsoft Dynamics 365 Commercessa.

## <a name="overview"></a>Yleiskuvaus


Dynamics 365 Commercessa puhelinpalvelukeskus on Commerce-tyyppinen kanava, joka voidaan määrittää sovelluksessa. Kun puhelinkeskusentiteeteille määritetään kanava, järjestelmä voi sitoa tietyt tiedot ja tilausten käsittelyn oletukset myyntitilauksiin. Yritys voi määrittää useita puhelinkeskuskanavia Commercessa. On kuitenkin tärkeää huomata, että yksittäinen käyttäjä voidaan linkittää vain yhteen puhelinkeskuskanavaan. 

Varmista ennen uuden puhelinkeskuskanavan luomista, että olet tehnyt valmiiksi [kanavan määrityksen edellytykset](channels-prerequisites.md).

## <a name="create-and-configure-a-new-call-center-channel"></a>Uuden puhelinkeskuskanavan luominen ja määrittäminen

Voit luoda ja määrittää uuden puhelinkeskuskanavan seuraavasti.

1. Siirry navigointiruudussa kohtaan **Vähittäismyynti ja kauppa \> Kanavat \> Puhelinkeskukset \> Kaikki puhelinkeskukset**.
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **Nimi**-kenttään uuden kanavan nimi.
1. Valitse avattavasta luettelosta sopiva **Yritys**.
1. Valitse avattavasta luettelosta sopiva **Varasto**-sijainti. Tätä sijaintia käytetään tälle puhelinkeskuskanavalle luotujen myyntitilausten oletusarvona, jos muita oletusarvoja ei ole määritetty asiakas- tai nimiketasolla.
1. Anna kelvollinen oletusasiakas **Oletusasiakas**-kentässä. Näitä tietoja käytetään automaattisen täytön oletusarvoissa, kun luodaan uusia asiakastietueita. Kun luodaan puhelinkeskuksen tilauksia, ei kannata luoda tilauksia oletusasiakkaalle.
1. Anna kelvollinen sähköpostin ilmoitusprofiili **Sähköposti-ilmoitusprofiili**-kentässä. Puhelinkeskustilausten luomisessa ja käsittelyssä käytetään sähköposti-ilmoituksen profiilia automaattisten sähköposti-ilmoitusten käynnistämisessä. Ne ilmoittavat asiakkaille tilauksen tilan.
1. Anna **Hinnan ohitus** -tietokoodi. Tämä tietokoodi on ehkä luotava ensin. Tämä tietokoodi sisältää niiden syykoodien joukon, joiden avulla käyttäjää pyydetään määrittämään hinnan ohituksen toiminto puhelinkeskustilauksessa.
1. Anna **Pitokoodi**-tietokoodi. Tämä tietokoodi on ehkä luotava ensin. Tämä tietokoodi sisältää niiden valinnaisten syykoodien joukon, joiden avulla käyttäjää pyydetään määrittämään tilauksen pitoon asettaminen.
1. Anna **Luotto**-tietokoodi. Tämä tietokoodi on ehkä luotava ensin. Tämä tietokoodi sisältää niiden syykoodien joukon, joiden avulla käyttäjä voi valita tilauksen kredit-toiminnon puhelinkeskuksesta muiden kuin hyvitysten antamiseksi asiakkaalle asiakaspalvelullisista syistä.
1. Valinnainen: Määritä taloushallinnon dimensiot **Taloushallinnon dimensiot** -pikavälilehdessä. Tässä annetut dimensiot ovat oletusarvoja kaikissa tässä puhelinkeskuskanavassa luoduissa myyntitilauksissa.
1. Valitse **Tallenna**.

Seuraavassa kuvassa näytetään, miten uusi puhelinkeskuskanava luodaan.

![Uusi puhelinkeskuskanava.](media/channel-setup-callcenter-1.png)

Seuraavassa kuvassa on esimerkki puhelinkeskuskanavasta.

![Esimerkki puhelinkeskuskanavasta.](media/channel-setup-callcenter-2.png)

## <a name="additional-channel-setup"></a>Lisäkanavan määrittäminen

Puhelinkeskuskanavan asetuksia varten tarvittavia tehtäviä, kuten maksutapojen ja toimitustapojen määrittäminen.

Seuraavassa kuvassa on **Asetukset**-välilehden **Toimitustavat**- ja **Maksutavat**-asetusvaihtoehdot.

![Puhelinkeskuskanavan lisämääritykset.](media/channel-setup-callcenter-3.png)

### <a name="set-up-payment-methods"></a>Maksutapojen määrittäminen

Voit määrittää maksutavan kullekin tässä kanavassa tuetulle maksutyypille seuraavien ohjeiden mukaisesti. Käyttäjien on valittava ennalta määritetyistä maksutavoista. Maksutapa linkitetään heille puhelinkeskuskanavassa. Ennen kuin määrität puhelinkeskuksen maksutavat, määritä päämaksutapa kohdassa **Vähittäismyynti ja kauppa \> Kanavan asetukset \> Maksutavat \> Maksutavat**.

1. Valitse toimintoruudussa ensin **Asetukset**-välilehti ja sitten **Maksutavat**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse siirtymisruudussa maksutapa käytettävissä olevista ennalta määritetyistä maksuista.
1. Määritä tarvittaessa maksutyypin mahdolliset lisäasetukset. Luottokorteille, lahjakorteille ja kanta-asiakkuuskorteille vaaditaan lisäasetukset. Valitse **Kortin asetukset** -toiminto. 
1. Määritä soveltuvat kirjaustilit maksutyypille **Kirjaus**-osassa.
1. Valitse toimintoruudussa **Tallenna**.

Seuraavassa kuvassa näkyy esimerkki käteismaksutavasta.

![Esimerkki maksutavoista.](media/channel-setup-callcenter-payments.png)

### <a name="set-up-modes-of-delivery"></a>Määritä toimitustavat

Määritetyt toimitustavat saadaan näkyviin valitsemalla **Toimitustapa** **toimintoruudun** **Asetukset**-välilehdessä.  

Voit muuttaa toimitustapaa tai lisätä sen ja liittää puhelinkeskuskanavaan seuraavasti.

1. Valitse puhelinkeskuksen toimitustapojen lomakkeessa **Hallitse toimitustapoja**
1. Luo uusi toimitustapa valitsemalla toimintoruudussa **Uusi** tai valitse aiemmin luotu tapa.
1. Lisää puhelinkeskuskanava valitsemalla **Vähittäismyyntikanava**-osassa **Lisää rivi**. Kanavien lisäämistä voi yksinkertaistaa käyttämällä organisaatiosolmua sen sijaan, että kukin kanava lisättäisiin erikseen.
1. Varmista, että toimitustapa on määritetty **Tuotteet**-pikavälilehden ja **Osoitteet**-pikavälilehden tietojen avulla. Jos tuotteet tai toimitusosoitteet eivät ole sallittuja toimitustavalle, sen valitseminen tilauksen syöttämisen aikana päättyy virheeseen.
1. Kun muutokset puhelikeskuksen toimitustilan määrityksiin on tehty muutokset, **Käsittele toimitustilat** -työ on suoritettava muutosmatriisi hajoittamiseksi. Tämä työ löytyy siirtymällä kohtaan **Vähittäismyynti ja kauppa \> Vähittäismyynnin ja kaupan IT \> Käsittele toimitustilat**.

Seuraavassa kuvassa on esimerkki toimitustavasta.

![Määritä toimitustavat.](media/channel-setup-retail-7.png)

### <a name="set-up-channel-users"></a>Kanavan käyttäjien määrittäminen

Voit luoda myyntitilauksen, joka on linkitetty puhelinkeskuskanavaan Commerce Headquarters -sovelluksesta, jos myyntitilauksen luonut käyttäjä on linkitetty puhelinkeskuskanavaan. Käyttäjä ei voi linkittää Commerce Headquarters -sovelluksessa luotua myyntitilausta manuaalisesti puhelinkeskuskanavaan. Linkki on systemaattinen. Se perustuu käyttäjään ja käyttäjän sekä puhelinkeskuskanavan suhteeseen. Käyttäjä voidaan linkittää vain yhteen puhelinkeskuskanavaan.

1. Valitse toimintoruudussa ensin **Kanava**-välilehti ja sitten **Kanavan käyttäjät**.
1. Valitse toimintoruudussa **Uusi**.
1. Valitse olemassa oleva **Käyttäjän tunnus** avattavasta valintaluettelosta ja linkitä tämä käyttäjä puhelinkeskuskanavaan

Kun kanavan käyttäjän määritys on valmis ja käyttäjä luo uuden myyntitilauksen Commerce Headquarters -sovelluksessa, myyntitilaus linkitetään liitettyyn puhelinkeskuskanavaan. Kaikki tämän kanavan määritykset kohdistetaan systemaattisesti myyntitilaukseen. Käyttäjä voi vahvistaa, mihin puhelinkeskuskanavaan myyntitilaus linkitetään, katsomalla kanavan nimen viitteen myyntitilauksen otsikosta.


### <a name="set-up-price-groups"></a>Hintaryhmien määrittäminen

Hintaryhmät ovat valinnaisia. Jos niitä käytetään, voidaan hallinnoida asiakkaille tilauksissa tarjottavia myyntihintoja puhelinkeskuskanavassa. Jos hintaryhmää ei ole määritetty asiakkaalle tai jos luettelon hintaryhmiä ei ole kohdistettu myyntitilaukseen (käyttämällä **Lähdekoodin tunnus** -kenttää puhelinkeskuksen tilauksen otsikossa), nimikkeiden hinnat määritetään käyttämällä kanavan hintaryhmää. Jos hintaryhmää ei löydy puhelinkeskuskanavasta, käytetään oletusnimikkeen päähintoja. 

Voit määrittää hintaryhmän seuraavasti.

1. Valitse toimintoruudussa ensin **Kanava**-välilehti ja sitten **Hintaryhmät**.
1. Napsauta Toimintoruudussa **Uusi**.
1. Valitse **Vähittäismyynnin hintaryhmä** avattavasta valintaluettelosta.

## <a name="additional-resources"></a>Lisäresurssit

[Kanavan määrittämisen edellytykset](channels-prerequisites.md)

[Puhelinkeskuksen myyntitoiminnot](call-center-functionality.md)

[Puhelinkeskuksen tilaustenkäsittelyasetusten määrittäminen](set-up-order-processing-options.md)

[Puhelinpalvelukeskuksen luettelot](call-center-catalogs.md)

[Petoshälytysten määrittäminen ja käyttäminen](set-up-fraud-alerts.md)

[Jatkuvuusohjelmien määrittäminen puhelinkeskuksille](set-up-continuity-program.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]