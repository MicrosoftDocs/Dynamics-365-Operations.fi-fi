---
title: Muistiinpanojen integrointi
description: Tässä artikkelissa kuvataan muistiinpanotietojen integraatiota kaksoiskirjoituksessa.
author: RamaKrishnamoorthy
ms.date: 02/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f09d455181b7929e25d5238949a0236ac60d457b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289013"
---
# <a name="note-integration"></a>Muistiinpanojen integrointi

[!include [banner](../../includes/banner.md)]



Liiketoimintaprosessien aikana Microsoft Dynamics 365 -käyttäjät usein keräävät tietoja asiakkaistaan. Nämä tiedot tallennetaan aktiviteetteina ja muistiinpanoina. Tässä artikkelissa kuvataan muistiinpanotietojen integraatiota kaksoiskirjoituksessa.

Asiakastiedot voidaan luokitella seuraavilla tavoilla:

+ **Toiminnan perustana toimivat iedot, joita Dynamics 365 -käyttäjä käsittelee asiakkaan puolesta** – Esimerkiksi Contoso (Dynamics 365 -käyttäjä) pitää pelinäytöksen. Yksi Contoson asiakkaista (asiakas) haluaa osallistua pelinäytökseen. Asiakas pyytää Contoso-työntekijää varaamaan paikan pelinäytökseen. Varaus tehdään Contoson tapahtuman osallistujan kalenterissa.
+ **Dynamics 365 -käyttäjän tiedot toiminnan pohjaksi** – Esimerkiksi Surface-yksikköä ostava asiakas määrittää erityisohjeet, jotka ilmaisevat, että laitteen tulee olla lahjapaketissa ennen toimitusta. Nämä ohjeet ovat toimintakelpoisia tietoja, joita pakkauksesta vastaavan Contoso-työntekijän tulisi käsitellä.
+ **Ei-toimittavissa olevat tiedot** – Asiakas esimerkiksi käy Contoso-myymälässä ja ilmaisee myyjälle kiinnostuksen *Halo*-peleihin ja -pelivälineisiin. Myyjä kirjoittaa nämä tiedot muistiinpanoihin. Tämän jälkeen tuotesuositusten ohjelma antaa asiakkaalle suosituksia tiedon perusteella.

Yleisesti ottaen toiminnalliset tiedot siepataan *aktiviteetteina* talous- ja toimintosovelluksissa sekä asiakasvuorovaikutussovelluksissa. Ei-toiminnalliset tiedot siepataan *muistiinpanoina* talous- ja toimintosovelluksissa sekä *huomautuksina* asiakasvuorovaikutussovelluksissa.

> [!TIP]
> Vaikka muistiinpanot on tarkoitettu ei-toimintakelpoisten tietojen käsittelemiseen, sovellukset eivät estä niiden käyttämistä toimintakelpoisten tietojen tallennukseen ja käsittelyyn, jos haluat käyttää niitä tällä tavalla.

Microsoft julkaisee parhaillaan muistiinpanojen integraation toiminnallisuutta. (Aktiviteettien integroinnin toiminnot julkaistaan myöhemmin.) Muistiinpanojen integrointi on käyettävissä asiakkaille, toimittajille, myyntitilauksille ja ostotilauksille.

## <a name="create-a-note-in-a-customer-engagement-app"></a>Muistiinpanon luominen asiakasvuorovaikutussovelluksessa

Noudattamalla seuraavia ohjeita voit luoda muistiinpanon asiakasvuorovaikutussovelluksessa sekä synkronoida sen sitten talous- ja toimintosovellukseen.

1. Avaa asiakkaan tilitietue asiakasvuorovaikutussovelluksessa.
2. Valitse **Aikajana**-ruudusta plusmerkki (**+**) ja luo muistiinpano valitsemalla **Muistiinpano**.

    ![Muistiinpanon luominen asiakasvuorovaikutussovelluksessa.](media/notes-ce-1.png)

3. Kirjoita otsikko ja kuvaus ja valitse sitten **Lisää muistiinpano**.

    ![Kirjoita otsikko ja kuvaus.](media/notes-ce-2.png)

    Uusi muistiinpano lisätään asiakkaan aikajanaan.

    ![Asiakkaan aikajanan uusi muistiinpano.](media/notes-ce-3.png)

4. Kirjaudu talous- ja toimintosovellukseen ja avaa sama asiakastietue. Huomaa, että oikeassa yläkulmassa oleva **Liitteet**-painike (paperiliitinsymboli) ilmaisee, että tietueella on liite.

    ![Ilmoitus liitteestä.](media/notes-ce-4.png)

5. Avaa **Liitteet**-sivu valitsemalla **Liitteet**-painike. Sinu pitäisi nähdä muistiinpano, jonka olet luonut asiakasvuorovaikutussovelluksessa.

    ![Muistiinpano asiakasvuorovaikutussovelluksesta.](media/notes-ce-5.png)

Muistiinpanon päivitykset synkronoidaan talous- ja toimintosovelluksen sekä asiakasvuorovaikutussovelluksen välillä.

## <a name="create-a-note-in-a-finance-and-operations-app"></a>Muistiinpanon luominen talous- ja toimintosovelluksessa

Voit luoda muistiinpanon myös talous- ja toimintosovelluksessa, ja se synkronoidaan sitten asiakasvuorovaikutussovellukseen.

Muistiinpano voidaan luoda seuraavasti talous- ja toimintosovelluksessa sekä synkronoida se sitten asiakasvuorovaikutussovellukseen.

1. Valitse talous- ja toimintosovelluksen **Liitteet**-sivulla **Uusi** \> **Muistiinpano**.

    ![Muistiinpanon luominen talous- ja toimintosovelluksessa.](media/notes-fo-1.png)

2. Kirjoita otsikko, lyhyt ohjejoukko ja valitse sitten **Tallenna**.

    ![Kirjoita otsikko ja ohjeet.](media/notes-fo-2.png)

3. Päivitä tietue asiakasvuorovaikutussovelluksessa. Uuden muistiinpanon pitäisi olla aikajanalla.

    ![Aikajanan uusi muistiinpano asiakasvuorovaikutussovelluksessa.](media/notes-fo-3.png)

Voit luokitella muistiinpanon sisäiseksi tai ulkoiseksi.

- Avaa talous- ja toimintosovelluksessa **Liitteet**-sivulla muistiinpano ja valitse sitten **Rajoitus**-kentästä **Sisäinen** tai **Ulkoinen**.

    ![Rajoituskenttä.](media/notes-fo-4.png)

Voit myös luoda URL-osoitteen.

1. Valitse talous- ja toimintosovelluksen **Liitteet**-sivulla **Uusi** \> **URL-osoite**.
2. Kirjoita otsikko ja URL-osoite.
3. Valitse **Rajoitus**-kentästä **Sisäinen** tai **Ulkoinen**.

    ![URL-osoitteen luominen talous- ja toimintosovelluksessa.](media/notes-fo-5.png)

4. Valitse **Tallenna**.

    Koska asiakasvuorovaikutussovelluksissa ei ole URL-tyyppiä, URL-osoite integroidaan kaksoiskirjoituksen avulla muistiinpanona.

    ![URL-osoitteen näkyminen asiakasvuorovaikutussovelluksessa.](media/notes-ce-6.png)

> [!NOTE]
> Tiedostoliitteitä ei tueta.

## <a name="templates"></a>Mallit

Muistiinpanojen integraatio sisältää taulukarttojen kokoelman, joita käytetään yhdessä tietojen vuorovaikutuksen aikana seuraavan taulukon mukaisesti.

| Talous- ja toimintosovellus | Asiakkaiden aktivointisovellus | Kuvaus |
|----------------------------|-------------------------|-------------|
| [Asiakkaan liitteet](mapping-reference.md#230) | Huomautukset | Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita asiakaskohtaisten tietojen keräämiseen (sekä organisaatioille että henkilöille). |
| [Toimittajan asiakirjaliitteet](mapping-reference.md#231) | Huomautukset | Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita toimittajakohtaisten tietojen keräämiseen (sekä organisaatioille että henkilöille). |
| [Myyntitilauksen otsikkoasiakirjan liitteet](mapping-reference.md#229) | Huomautukset | Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita myyntitilauskohtasten tietojen sieppaamiseen. |
| [Ostotilauksen otsikkoasiakirjan liitteet](mapping-reference.md#232) | Huomautukset | Yritykset, jotka käyttävät tavallista tekstiä ja URL-osoitteita ostotilauskohtaisten tietojen sieppaamiseen. |

## <a name="limitations"></a>Rajoitukset

Kun olet asentanut huomautusratkaisun, sen asennusta ei voi poistaa. 

Lisätietoja on [kaksoiskirjoituksen yhdistämismäärityksen viitteessä](mapping-reference.md).

