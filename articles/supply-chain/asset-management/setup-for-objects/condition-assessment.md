---
title: Kunnon arviointi
description: Tässä ohjeaiheessa kerrotaan, kuinka voit luoda kuntoarviointimallin ja rekisteröinnin resurssiin resurssien hallinnassa.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05d1a38ab8de406a1615c474ffe39d231335fb67
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570050"
---
# <a name="condition-assessment"></a>Kunnon arviointi

[!include [banner](../../includes/banner.md)]

 

Tässä ohjeaiheessa kerrotaan, kuinka voit luoda kuntoarviointimallin ja rekisteröinnin resurssiin resurssien hallinnassa. Kunnon arviointi suoritetaan säännöllisin väliajoin, ja ensisijaisena tavoitteena on luoda ja ylläpitää resurssien kuntotietoja. Ennakoivan kunnossapidon näkökulmasta katsottuna on tärkeää valvoa keskeisiä tietoja, kuten nykykuntoa ja jäljellä olevaa elinikää. Lisäksi, jos teet kunnon arvioinnin säännöllisin väliajoin, pystyt seuraamaan ja vertailemaan tehtaasi koneiden kuntoa.

Kunnon arvioinnin avulla voidaan mitata ja valvoa monia laitteiston kunnon osa-alueita. Esimerkki: Voit mitata koneen tärinää. Kun olet rekisteröinyt resurssien hallinnassa värähtelymittauksia erityyppisille laitteille, voit etsiä viimeisintä rekisteröityä arviointia ja tarkastella tärinän mittauksia.

Kunnon arvioinnit luodaan resursseille. Voit määrittää kuunon arviointimallin resurssityypille ennen kuntoarviointimenettelyn suorittamista. Syy arviointimallien käyttämiseen on välttää samanlaisiin resursseihin kuuluvien kuntotietojen vaihtelu. Kunnon arvioinnin määrittäminen ja käyttäminen järjestys resurssien hallinnassa on: ensin määritetään tarvittavat kunnon arviointimallit. Liitä seuraavaksi mallit liitetään resurssityyppeihin **Resurssityypit**-lomakkeessa. Lopuksi voit luoda kunnon arvioinnin rekisteröinnit resurssille **resurssi**-lomakkeessa.

## <a name="create-a-condition-assessment-template"></a>Luo kunnon arviointimalli

1. Valitse **resurssien hallinta** > **Asetukset** > **resurssityypit** > **Kunnon arviointi**.
2. Luo uusi malli valitsemalla **Uusi**.
3. Kirjoita **Malli**-kenttään mallin tunnus.
4. Kirjoita **Nimi**-kenttään mallin nimi.
5. Lisää **Kunnon arviointirivit** -pikavälilehdessä kunnon arviointiin tarvittavat rivit, mukaan lukien asianmukaisen kuntotyypin ja mittayksikön valinta.
6. Lisää **resurssityypit**-pikavälilehdessä resurssityypit, joiden tulisi käyttää kunnon arviointimallia.
7. Näytön yläreunassa olevan **Tiedot** -ryhmän kentissä **rivit** ja **resurssityypit** näkyy valittuun kunnon arviointimalliin liittyvien arviointirivien ja resurssityyppien määrä.


## <a name="create-condition-assessment-registration-on-an-asset"></a>Luo resurssille kunnon arvioinnin rekisteröinti

1. Valitse **Resurssien hallinta**  >  **Yhteiset**  >  **Resurssit**  >  **Kaikki resurssit**.
2. Valitse luettelosta resurssi, jolle haluat luoda kunnon arvioinnin rekisteröinnin.
3. Valitse **Yleiset**-välilehdestä **Kunnon arviointi**.
4. Lisää uusi rekisteröinti valitsemalla **Uusi**.
5. Valitse kunnon arvioinnin päivämäärä **Päivämäärä**-kentässä.
6. Valitse työntekijä, joka suoritti arvioinnin rekisteröinnin **Työntekijä**-kentässä.
7. **Rivit**-kentässä näkyy kunnon arviointiin asetettujen arviointirivien määrä.
8. Valitse kunnon arvioinnin malli **Malli**-kentässä. Mallin nimi lisätään automaattisesti **nimi**-kenttään, ja siihen liittyvät rekisteröintirivit lisätään **Kunnon arviointirivit** -pikavälilehteen.
9. Voit lisätä valittuun kunnon arviointiin liittyviä muistiinpanoja **Huomautukset**-pikavälilehdessä.
10. Lisää jokaiselle kunnon arviointiriville mittaustiedot **Arvo**-kenttään.
11. Voit lisätä valittuun rekisteröintiriviin liittyvän kommentin **Kunnon arviointirivit** -pikavälilehden**Kommentit**-kenttään. Jos lisäät riville kommentin, **Kommentti**-valintaruutu valitaan automaattisesti.

Kun olet tehnyt kunnon arvioinnin rekisteröinnin resurssille, voit tulostaa kunnon arviointiraportin.

>[!NOTE]
>Voit myös rekisteröidä kunnon arvioinnintyötilaukselle (**resurssien hallinta** > **Yhteiset** > **Työtilaukset** > **Kaikki työtilaukset** > **Kunnon arviointi** -painike).
