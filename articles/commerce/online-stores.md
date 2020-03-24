---
title: Määritä verkkokauppakanava
description: Tässä artikkelissa on tietoja verkkokauppakanavista ja niiden määrittämisestä Dynamics 365 Commerceissa.
author: kfend
manager: AnnBe
ms.date: 03/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelManagementWorkspace, RetailOnlineStoreList
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b719e40720b091eec879edf332ab63db710a1ebc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096891"
---
# <a name="set-up-an-online-store-channel"></a>Määritä verkkokauppakanava

[!include [banner](includes/banner.md)]

Tässä artikkelissa on tietoja verkkokauppakanavista ja niiden määrittämisestä Dynamics 365 Commerceissa.

Commerce tukee useita vähittäismyynnin kanavia. Kanavia ovat verkkokaupat, puhelinkeskukset ja vähittäismyymälät (eli kivijalkakaupat). Verkkokaupassa vähittäismyyjät saavat näkyvyyttä Internetissä, ja asiakkaat voivat ostaa tuotteita sekä verkkokaupasta että vähittäismyymälästä. Verkkokaupasta tuotteita ostavat asiakkaat voivat saada tuotteet kotiin toimitettuina tai noutaa ne paikallisesta myymälästä. 

Luot verkkokaupan Commerce-asiakasohjelmassa. Verkkokauppa julkaistaan kolmannen osapuolen verkkokaupassa, joka on yhdistetty Commerceen. Kolmannen osapuolen verkkokauppa toimii verkkokauppasi edustana (käyttöliittymänä), ja voit valita haluamasi asiakkuudenhallintajärjestelmän ja käyttöliittymäominaisuudet. Käytettävissä useita tämäntyyppisiä integrointivaihtoehtoja. 

Verkkokaupalle määritetyt ominaisuudet ohjaavat verkkokaupan toimintoja. Esimerkki: Määrittelet siirtymisluokan hierarkian ja määrität sen verkkokaupalle. Kun julkaiset verkkokaupan kolmannen osapuolen verkkokaupassa, siirtymisluokan hierarkia näkyy kaupan verkkoversiossa. Ostajat voivat selata verkkokauppaa ja hakea tuotteita siirtymisluokan hierarkian avulla. 

Jos haluat luoda verkkokaupan, sinun on määritettävä kaupalle komponentit, jotka mahdollistavat tapahtumien käsittelyn. Sinun täytyy lisätä esimerkiksi valikoimat, määritteet, maksutavat ja toimitustavat. Voit määrittää hinnat, kampanjat, alennukset, alennukset, kauppasopimukset ja lähetyksen ehtoja, jotka liittyvät Internet-kauppa. 

Kun olet julkaissut verkkokauppasi kolmannen osapuolen verkkokaupassa, voit luoda sille tuoteluetteloita. Luettelon tuotteista tulee verkkokaupassa tuoteluetteloita. Kun asiakas ostaa tuotteita verkkokaupasta, saatavilla oleva varasto päivittyy ja synkronoituu asiakasohjelmassa. Lisäksi ostoille luodaan myyntitilaukset ja ne lähetetään asiakasohjelmaan tilauksen toimitusta ja käsittelyä varten.

## <a name="set-up-an-online-store"></a>Perusta online-kauppa

Kun perustat verkkokauppaa, tee seuraavat tehtävät:

1. Luo verkkokauppa.
2. Lisää verkkokauppa sopiviin organisaatiohierarkioihin.
3. Lisää tuotevalikoimat, joihin kuuluvat verkkokaupassa saatavilla olevat tuotteet.
4. Määritä tai luo hintaryhmät verkkokauppaa varten.
5. Määritä verkkokaupassa käytettävissä oleva toimitustavat.
6. Määritä maksutavat, jotka verkkokauppa hyväksyy.
7. Jos sallit ostajille tuotteiden Internet-tilaukset ja niiden keräyksen paikallisessa myymälässä, määritä verkkokaupalle toimipaikkapaikannin.
8. Määritä kanavien, tuotteiden ja myyntitilausten määritteet verkkokaupalle. Kanavamääritteet koskevat koko verkkokauppaa, tuotemääritteet koskevat verkkokaupan tuotteita ja myyntitilauksen määritteet koskevat verkkokaupassa luotuja myyntitilauksia.
9. Yhdistämällä määritteitä voit määritellä ominaisuuksia, jotka ohjaavat sitä, miten kyseiset määritteet toimivat verkkokaupassa. Määritteet voidaan asettaa esimerkiksi pakollisiksi tai haettaviksi.
10. Julkaise verkkokauppa, jotta voit luoda kaupan rakenteen valitsemaasi kolmannen osapuolen verkkokauppaan.

    > [!IMPORTANT]
    > Ennen verkkokaupan julkaisemista sille täytyy määrittää jakelusijainti.

## <a name="commerce-channel-navigation-hierarchies"></a>Commerce-kanavan siirtymishierarkiat

Määritä ennen verkkokaupan luomista siinä käytettävä Commerce-kanavan siirtymishierarkia. Kanavan siirtymishierarkia vastaa luokkahierarkiaa, joka näytetään verkkokaupassa kaupan julkaisemisen jälkeen. Kun julkaiset tuoteluetteloita verkkokaupassa, luettelon tuotteet yhdistetään kanavan siirtymishierarkian luokkiin. Ostajat voivat siirtyä verkkokaupassa hierarkian avulla.

## <a name="organization-hierarchies"></a>Organisaatiohierarkiat

Organisaatiohierarkioita käytetään kaupan kanavien rakenteeseen ja edustamaan yritystäsi muodostavien organisaatioiden välisiä suhteita. Kun perustat Internet-kauppoja, voit lisätä ne organisaatiohierarkiaan. Myymälät jakavat sitten valikoimissa, täydennyksissä ja raportoinnissa käytettävät tiedot. 

Luodessaan organisaatiohierarkian sinun on määritettävä sen tarkoitus. Tarkoitus kuvaa, kuinka hierarkiaa käytetään liiketoimintarakenteessa. Voit luoda yhden organisaatiohierarkian myymälän toimintoihin ja käyttää tätä hierarkiaa valikoimiin, täydennykseen ja raportointia varten. 

Vaihtoehtoisesti voit luoda erillisen organisaatiohierarkian jokaista käyttötarkoitusta varten. Voit myös luoda useita hierarkioita samaan tarkoitukseen ja määrittää jokaiselle erillisen kanavan. Jos aiot julkaista tuoteluetteloita verkkokaupassa, sinun on vähintään lisättävä verkkokauppa organisaatiohierarkiaan valikoimia varten. Luettelon tuotteet valitaan tuotevalikoimista, jotka on määritetty verkkokauppaan. Kun luettelo on julkaistu, julkaisuprosessi vertaa verkkokauppaan liitetyn valikoiman voimassaolopäiviä luettelossa oleviin tuotteisiin selvittääkseen, mitkä tuotteet tulisi antaa saataville verkkokaupassa.

## <a name="additional-resources"></a>Lisäresurssit

[Toimialueen nimen määrittäminen](configure-your-domain-name.md)

[Uuden sähköisen kaupankäynnin sivuston käyttöönotto](deploy-ecommerce-site.md)

[Sähköisen kaupankäynnin sivuston luominen](create-ecommerce-site.md)

[Liitä verkkosivusto kanavaan](associate-site-online-store.md)

[Robots.txt-tiedostojen hallinta](manage-robots-txt-files.md)

[URL-osoitteen uudelleenohjausten lataaminen joukkona](upload-bulk-redirects.md)

[B2C-vuokraajan määrittäminen Commercessa](set-up-B2C-tenant.md)

[Mukautettujen sivujen määrittäminen käyttäjän kirjautumisia varten](custom-pages-user-logins.md)

[Useiden B2C-vuokraajien määrittäminen Commerce-ympäristössä](configure-multi-B2C-tenants.md)

[Sisältöverkon (CDN) tuen lisääminen](add-cdn-support.md)

[Sijaintiin perustuvan myymälän tunnistuksen käyttöönotto](enable-store-detection.md)
