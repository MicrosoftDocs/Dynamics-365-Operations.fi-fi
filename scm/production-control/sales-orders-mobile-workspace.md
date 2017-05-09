---
title: "Myyntitilausten mobiili työtila Microsoft Dynamics 365 for Operations -sovellusta varten"
description: "Myyntitilausten mobiilin työtilan avulla pysyt ajan tasalla myyntitilauksistasi missä ja milloin tahansa."
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

# <a name="sales-orders-mobile-workspace-for-microsoft-dynamics-365-for-operations-app"></a>Myyntitilausten mobiili työtila Microsoft Dynamics 365 for Operations -sovellusta varten

Myyntitilausten mobiilin työtilan avulla pysyt ajan tasalla myyntitilauksistasi missä ja milloin tahansa. 

<a name="prerequisites"></a>Edellytykset
-------------

| Edellytys                                                         | kuvaus                                                                                                                                                                   |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Lue Microsoft Dynamics 365 for Operations -mobiiliympäristöstä | [Dynamics 365 for Operations -mobiiliympäristö](/dynamics365/operations/dev-itpro/mobile-apps/mobile-platform)                                                              |
| Dynamics 365 for Operations                                          | Varmista, että käytössäsi on ympäristö, johon on asennettu Microsoft Dynamics 365 for Operations -versio 1611 sekä Microsoft Dynamics for Operations ympäristöpäivitys 3 (Marraskuu 2016). |
| Hotfix-korjaus KB 3215650                                                    | Asenna korjaustiedosto ottaaksesi käyttöön työtilat, jotka toimitetaan Microsoft Dynamics 365 for Operationsissa.                                                                       |
| Mobiililaite, johon on asennettu Dynamics 365 for Operations -sovellus | Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.                                                                                                      |

## <a name="overview"></a>Yleiskuvaus
Mobiili työtila yhdistää Dynamics 365 for Operations -sovellukseen, ja sen avulla voit tarkastella yksityiskohtaisia tietoja kustakin myyntitilauksesta, kuten tilauksen tilan, asiakkaan yhteystiedot ja tilauksen vastaanottajan yhteystiedot. Mobiilissa työtilassa on pikanäyttö myyntitilauksista. Voit tarkastella myyntitilauksia asiakaskohtaisesti, näyttää kaikki myyntitilaukset tai tarkastella yksittäisen myyntitilauksen tietoja. Mobiili työtila tarjoaa kaksi näkymää, joilla voit analysoida myyntitilausten yksityiskohtia.

### <a name="view-all-sales-orders"></a>Näytä kaikki myyntitilaukset

Tämä näkymä sisältää kaikki myyntitilaukset.

-   Valitse tarkasteltavat myyntitilaukset seuraavien suodattimien avulla.
    -   Etsi myyntitilauksen perusteella
    -   Etsi asiakastilin perusteella
    -   Etsi asiakkaan nimen perusteella
    -   Etsi tilan perusteella
    -   Etsi vapautustilan perusteella
    -   Etsi luontipäivämäärän ja -ajan perusteella

<!-- -->

-   Kun olet valinnut myyntitilaukset, voit tarkastella tiettyjen tilausten lisätietoja. Tarkasteltavana on erityisesti:
    -   Asiakkaan nimi ja osoitetiedot
    -   Myyntitilauksen eri päivät, kuten pyydetty lähetyspäivämäärä ja vahvistettu lähetyspäivämäärä.
    -   Tilauksen vastaanottajan yhteystiedot
    -   Asiakkaan yhteystiedot
    -   Tilausrivit
    -   Lähetykset, joista näet miten ja milloin myyntitilaus on toimitettu

### <a name="view-orders-for-a-customer-"></a>Tarkastele asiakkaan tilauksia** **

Tässä näkymässä on asiakaskohtainen luettelo myyntitilauksista.

-   Voit tarkastella asiakkaan myyntitilauksia seuraavien suodattimien avulla.
    -   Etsi nimen perusteella
    -   Etsi tilin perusteella

<!-- -->

-   Kun olet valinnut asiakkaan, tarkasteltavana on:
    -   Asiakkaan nimi ja ryhmä
    -   Asiakkaan yhteystiedot
    -   Asiakkaan myyntitilaukset ja tilausten tiedot:
        -   Asiakkaan nimi ja osoitetiedot
        -   Myyntitilauksen eri päivämäärät
        -   Tilauksen vastaanottajan yhteystiedot
        -   Asiakkaan yhteystiedot
        -   Tilausrivit
        -   Lähetykset, joista näet miten ja milloin myyntitilaukset on toimitettu

## <a name="get-started"></a>Aloittaminen
Aloita myyntitilausten mobiilin työtilan käyttö mobiililaitteellasi seuraamalla näitä ohjeita.

1.  Lataa mobiilisovelluskaupasta Microsoft Dynamics 365 for Operations -sovellus.
2.  Käynnistä sovellus laitteessa.
3.  Anna Dynamics 365 -URL-osoitteesi.
4.  annan yritys, johon kirjaudutaan. Kirjoita esimerkiksi **USMF**.
5.  Ensimmäinen kerta, kun kirjaudut sisään, sinulta pyydetään Microsoft Dynamics 365 for Operations -tilisi käyttäjänimeä ja salasanaa. Kirjota tunnistetiedot. Kun olet kirjautunut sisään, näet yrityksen käytettävissä olevat työtilat.

Jotta voit tarkastella mobiilisovelluksessa työtiloja, halutut työtilat on ensin julkaistava Dynamics 365 for Operationsiin.

1.  Käynnistä Dynamics 365 for Operations.
2.  Valitse **Järjestelmän hallinta** &gt; **Asetukset** &gt; **järjestelmän parametrit**.
3.  Valitse **Hallitse mobiilisovellusta**.
4.  Valitse työtila julkaistaksesi mobiiliympäristöön.
5.  Valitse **Julkaise työtila**.
6.  Päivitä laitteesi nähdäksesi julkaistut työtilat.

## <a name="view-information-about-sales-orders-for-a-customer"></a>Näytä tietoja asiakkaan myyntitilauksista
1.  Valitse mobiililaitteessasi **Myyntitilaukset** -työtila.
2.  Valitse **Tarkastele asiakkaan tilauksia**.
3.  Etsi haluamasi asiakas **Tili **tai **Asiakkaan nimi ** -tietojen avulla.
4.  Valitse asiakas.
5.  Valitse **Yhteystiedot** tai **Myyntitilaukset**.
6.  Jos valittuna on **Myyntitilaukset**, näyttöön tulee luettelo asiakkaan myyntitilauksista.
7.  Valitse **Myyntitilaus**.
8.  Tässä kentässä voit tarkastella tietoja myyntitilausriveistä, toimituksista, asiakkaan yhteystiedoista ja tilauksen vastaanottajan yhteystiedoista.




