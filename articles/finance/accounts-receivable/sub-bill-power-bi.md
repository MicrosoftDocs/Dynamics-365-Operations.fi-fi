---
title: Tilauslaskutuksen käytön Power BI -sisältö
description: Tässä artikkelissa käsitellään tilauslaskutuksen Microsoft Power BI -sisältöä.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849957"
---
# <a name="subscription-billing-power-bi-content"></a>Tilauslaskutuksen käytön Power BI -sisältö

[!include[banner](../includes/banner.md)]

Tässä artikkelissa käsitellään tilauslaskutuksen Microsoft Power BI -sisältöä. Siinä selitetään, miten sisältyvät Power BI -raportit avataan, sekä kerrotaan sisällön muodostamisessa käytetyistä tietomallista ja yksiköistä. 

## <a name="overview"></a>Yleiskuvaus

Tilauslaskutuksen Power BI -sisältö luotiin tilauslaskutuksen laskuttajien ja päälliköiden käyttöön. Se tarjoaa tilauslaskutuksen tärkeimmät mittaustiedot, kuten laskutusaikataulujen kuukausittaisen toistuvan tuoton sekä lykkäysaikataulujen vähenevän saldon ja vesiputousmallin tiedot. Se antaa yhteenvedon toistuvista tuloista ja tuotoista laskutusaikataulujen ja lykkäysaikataulujen tietojen avulla.

Power BI -sisällön kolme välilehteä ovat seuraavat, ja niiden avulla saadaan neljä analyyttista raporttia: 

- **Analytiikka - MRR** – Tämä välilehti sisältää **Kuukausittaisen toistuvan laskutuksen** raportin ja **Laskutusaikataulun erittely** -raportin.
- **Analytiikka – vesiputousmalli** – Tämä välilehti sisältää **Tuoton vesiputousmalli** -raportin.
- **Analytiikka – vähenevä saldo** – Tämä välilehti sisältää **vähenevä saldo** -raportin.

## <a name="view-data-on-the-analytical-reports"></a>Analyyttisten raporttien tietojen tarkasteleminen

Ennen kuin voit tarkastella analyyttisten raporttien tietoja, sinun on suoritettava kausittainen prosessi, joka luo raportointitiedot kutakin raporttia varten. Nämä tiedot, joita raportit edellyttävät, on luotava, koska tietoja ei tallenneta suoraan tietokantaan. 

1. Siirry kohtaan **Tilauslaskutus \> Toistuvan sopimuksen laskutus \> Kausittaiset tehtävät \> MRR-analyysiraportin eräkäsittely**, ja toimi seuraavasti:

    1. Anna päivämääräväli, joka on enintään kolme vuotta.
    2. Valinnainen: Määritä toistuva eräkäsittelytyö tietojen kausittaista päivitystä varten.
    3. Valitse **OK**.

2. Kun erätyö on suoritettu loppuun, siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Yksikkösäilö** ja päivitä **MRR-raportin** koostemittari. 
3. Siirry kohtaan **Tilauslaskutus \> Tuotto- ja kululykkäykset \> Kausittaiset tehtävät \> Vesiputousmalli-analytiikkaraportin eräkäsittely**, ja toimi seuraavasti:

    1. Määritä alkamis- ja päättymispäivämäärä, joiden väli on enintään 26 kautta. 
    2. Jos haluat tarkastella nykyisen kauden menneiden kausien aikana ennustettua summaa, määritä **Ennusta aiemmat summat nykyiselle kaudelle** -arvoksi **Kyllä**.
    3. Valinnainen: Määritä toistuva eräkäsittelytyö tietojen kausittaista päivitystä varten.
    4. Valitse **OK**. 

4. Kun erätyö on suoritettu loppuun, siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Yksikkösäilö** ja päivitä **Vesiputousmalli-raportin** koostemittari.
5. Siirry kohtaan **Tilauslaskutus \> Tuotto- ja kululykkäykset \> Kausittaiset tehtävät \> Laskevan saldon analytiikkaraportin eräkäsittely**, ja toimi seuraavasti:

    1. Määritä alkamis- ja päättymispäivämäärä, joiden väli on enintään 26 kautta. 
    2. Jos haluat tarkastella nykyisen kauden menneiden kausien aikana ennustettua summaa, määritä **Ennusta aiemmat summat nykyiselle kaudelle** -arvoksi **Kyllä**.
    3. Valinnainen: Määritä toistuva eräkäsittelytyö tietojen kausittaista päivitystä varten.
    4. Valitse **OK**.

6. Kun erätyö on suoritettu loppuun, siirry kohtaan **Järjestelmän hallinta \> Asetukset \> Yksikkösäilö** ja päivitä **Laskevan saldon raportin** koostemittari.

## <a name="accessing-the-power-bi-content"></a>Power BI -sisällön käyttäminen

Tilauslaskutuksen Power BI -sisältö näkyy **Tilauslaskutus** -työtilassa.
