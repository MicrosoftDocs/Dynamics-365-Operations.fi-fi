---
title: "Myyntitilausten mobiili työtilaa varten Microsoft Dynamics-365 toiminnot app"
description: "Myyntitilausten mobiili-työtilan kanssa saat uusimmat myyntitilauksissa että missä tahansa ja milloin tahansa."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267134
ms.assetid: dbc6dc39-b535-42d3-9fbd-4724597388ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 7a0a2af2094e3e5be757d3dd82255769677b96ea
ms.openlocfilehash: 851c53e1c53fb37488ed86e25e3ede83ca0541db
ms.lasthandoff: 03/31/2017


---

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Myyntitilausten mobiili työtilaa varten Microsoft Dynamics-365 toiminnot app

Myyntitilausten mobiili-työtilan kanssa saat uusimmat myyntitilauksissa että missä tahansa ja milloin tahansa. 

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                         | kuvaus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lue Microsoft Dynamics-365 toimintojen mobiilien | [Toimintojen mobiilien Dynamics 365](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Työvaiheiden Dynamics 365                                          | Muista, että käytät ympäristössä, jossa on Microsoft Dynamics-365-version toimintoja 1611 ja päivittää toimia ympäristön Microsoft Dynamics 3 (marraskuu-2016). |
| Hotfix-korjauksen kt 3215650                                                    | Asentaa korjaustiedoston käyttöön työtilat, jotka toimitetaan Microsoft Dynamics-365 operaatioille.                                                                       |
| Kannettava laite, joka on asennettu toiminnot app for Dynamics-365 | Lataa mobile app myymälä toiminnot app for Dynamics-365.                                                                                                      |

## <a name="overview"></a>Yleiskuvaus
Tämän työtilan mobiili käyttää Dynamics-365-sovelluksen toimintoja ja avulla voit tarkastella yksityiskohtaisia tietoja kunkin myyntitilauksen, kuten tila, asiakkaan yhteystiedot ja tilauksen saajan yhteystiedot. Mobile workspace sisältää myyntitilaukset instant tutkimuksen. Voit tarkastella myyntitilauksia asiakkaan mukaan Näytä kaikki myyntitilaukset tai tarkastella tietoja tietyn myyntitilauksen. Mobile workspace tarjoaa kaksi näkymää haluat analysoida yksityiskohtaisesti myyntitilaukset.

### <a name="view-all-sales-orders"></a>Näytä kaikki myyntitilaukset

Tämä näkymä näyttää kaikki myyntitilaukset.

-   Käyttää seuraavien suodattimien valitsemiseen, jotka haluat tarkastella myyntitilauksia.
    -   Hae myyntitilauksen perusteella
    -   Etsi asiakkaan mukaan
    -   Hae asiakkaan nimen perusteella
    -   Etsi tilan mukaan
    -   Vapauta tilaa etsiä
    -   Etsiä luonnin päivämäärä ja aika

<!-- -->

-   Kun olet valinnut myyntitilauksia, voit tarkastella tiettyjen tilausten lisätietoja. Voit tarkastella erityisesti:
    -   Asiakkaan nimen ja osoitteen tiedot
    -   Toinen myyntitilaus päivämääriä, kuten pyydetty lähetyspäivä ja vahvistettu lähetyspäivä
    -   Tilauksen saajan yhteystiedot
    -   Asiakkaan yhteystiedot
    -   Tilausrivit
    -   Lähetykset, jotka osoittavat, miten ja milloin myyntitilaus toimitetaan

### <a name="view-orders-for-a-customer-"></a>Voit tarkastella tilauksia, asiakkaan ** **

Näkymä Luetteloi myyntitilaukset asiakkaittain.

-   Jokin seuraavien suodattimien avulla voit tarkastella asiakkaan.
    -   Hae nimen perusteella
    -   Etsi tilin mukaan

<!-- -->

-   Kun olet valinnut asiakas, voit tarkastella:
    -   Asiakkaan nimi ja ryhmä
    -   Asiakkaan yhteystiedot
    -   Asiakkaan myyntitilausten ja ostotilausten tietoja:
        -   Asiakkaan nimen ja osoitteen tiedot
        -   Myyntitilauksen eri päivämäärät
        -   Tilauksen saajan yhteystiedot
        -   Asiakkaan yhteystiedot
        -   Tilausrivit
        -   Lähetykset, jotka osoittavat, miten ja milloin Myynti tilaukset on toimitettu

## <a name="get-started"></a>Aloittaminen
Matkaviestimen käytön myyntitilausten mobile workspace seuraavasti.

1.  Mobile app-myymälä, lataa ja asenna toiminnot app for Microsoft Dynamics-365.
2.  Käynnistä sovellus laitteen.
3.  Anna URL-osoitteesi Dynamics 365.
4.  Kirjoita Kirjaudu yritys. Esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinua pyydetään käyttäjänimeä ja salasanaa Microsoft Dynamics-365, tilin toimintoja varten. Anna tunnistetietosi. Kun kirjaudut sisään, näet yrityksen käytettävissä olevat työtilat.

Voit tarkastella mobiili sovellusten työtilat, haluttu työtilat on ensin julkaistava toiminnot app for Dynamics-365.

1.  Käynnistä Dynamics 365 operaatioille.
2.  Siirry **järjestelmän hallinta**&gt;**asennus**&gt;**järjestelmäparametrit**.
3.  Valitse **hallinta mobile app**.
4.  Valitse työtila julkaista mobile platform.
5.  Valitse **julkaista työtilan**.
6.  Päivitä laitteesi on julkaistu työtilat.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Voit tarkastelutietoja asiakkaan myyntitilaukset
1.  Matkaviestimessä, valitse **myyntitilaukset** työtila.
2.  Valitse **tarkastella asiakkaan tilauksia**.
3.  Käytä ** tilin ** tai ** asiakkaan nimi ** tiedot Etsi haluttu asiakas.
4.  Valitse asiakas.
5.  Valitse **yhteystiedot** tai **myyntitilausten**.
6.  Jos **myyntitilausten** on valittu, asiakkaan myyntitilausten luettelo tulee näkyviin.
7.  Valitse **myynti**.
8.  Tässä kentässä voit tarkastella tietoja myyntitilausrivien, toimitukset, asiakkaan yhteystiedot ja tilauksen saajan yhteystiedot.




