---
title: Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä
description: Tässä artikkelissa käsitellään myymälöiden ja niitä vastaavien ryhmien määritystä Dynamics 365 Commerce headquartersissa, jos organisaatio on jo luonut ryhmiä Microsoft Teamsissa ennen Commerce-integrointia.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 67a1a79dd74d411aa7e21000c8baaa8a069cede7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: fi-FI
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279116"
---
# <a name="map-stores-and-teams-if-there-are-pre-existing-teams-in-microsoft-teams"></a>Myymälöiden ja tiimien yhdistämismääritykset, jos Microsoft Teamsissa on ennestään tiimejä

[!include [banner](includes/banner.md)]

Tässä artikkelissa käsitellään myymälöiden ja niitä vastaavien ryhmien määritystä Dynamics 365 Commerce headquartersissa, jos organisaatio on jo luonut ryhmiä Microsoft Teamsissa ennen Commerce-integrointia.

Organisaatiossasi voi olla ryhmiä luotuja joihinkin tai kaikkiin myymälöihin ennen Dynamics 365 Commercen ja Microsoft Teamsin integroimista. Tässä tapauksessa voit määrittää Commerce-myyntipisteen ja Microsoft Teamsin välisen tehtävän synkronoinnin antamalla myymälöiden ja vastaavien tiimien määritykset Commerce headquartersissa.

## <a name="map-stores-and-corresponding-teams-in-commerce-headquarters"></a>Myymälöiden ja vastaavien ryhmien määritys Commerce headquarters -sovelluksessa 

Tee myymälöiden ja vastaavien ryhmien määritys Commerce headquarters -sovelluksessa seuraavasti.

1. Valitse **Järjestelmänhallinta \> Työtila \> Tietojen hallinta**.
1. Valitse **Vie**. 
1. Valitse toimintoruudussa **Uusi**.
1. Kirjoita **ryhmän nimeksi** "Vie Teamsin määritys".
1. Valitse **Valitut yksiköt** -välilehdessä **Lisää yksikkö**. **Lisää yksikkö** -valintaikkuna tulee näkyviin.  
1. Valitse avattavasta **Yksikön nimi** -luettelosta **Teams-määritys lähteen ja ryhmän välillä**.
1. Valitse avattavasta **Kohdetietomuoto**-luettelosta **CSV**.
1. Valitse **Lisää** ja valitse sitten **Sulje**.
1. Valitse toimintoruudun vasemmassa yläreunassa **Vie nyt**.
1. Valitse **Yksikön käsittelyn tila** -kohdasta **Lataa tiedosto**.
1. Syötä vietyy CSV-tiedostoon arvot kohtiin **SOURCETYPE**, **SOURCEID** ja **TEAMID** seuraavasti:
    - Anna kohdassa **SOURCETYPE** arvo "RetailStore". 
    - Kirjoita kohdassa **SOURCEID** myymälän numero (esimerkiksi San Franciscon myymälän numeroksi "000135"). Myymälän numerot löytyvät kohdasta **Retail ja Commerce \> Kanavat \> Myymälät**.
    - Määritä **TEAMID**-kohtaan vastaava ryhmätunnus Microsoft Teamsista (esimerkiksi 5f8bc92b-6aa8-451e-85d1-3949c01ddc6c). Löydät ryhmätunnustiedot kohdasta [admin.teams.microsoft.com](https://admin.teams.microsoft.com).
1. Tallenna CSV-tiedosto paikalliseen tietokoneeseen.
1. Valitse **Järjestelmänhallinta \> Työtila \> Tietojen hallinta** ja valitse **Tuo**.
1. Valitse **Valitut yksiköt** -välilehdessä **Lisää tiedosto**. **Lisää tiedosto** -valintaikkuna tulee näkyviin.
1. Valitse avattavasta **Yksikön nimi** -luettelosta **Teams-määritys lähteen ja ryhmän välillä**.
1. Valitse avattavasta **Lähdetietomuoto**-luettelosta **CSV**.
1. Valitse **Lataa palvelimeen ja lisää**, valitse aiemmin tallentamasi CSV-tiedosto ja valitse sitten **Avaa**.
1. Valitse **Lisää tiedosto** -valintaikkunassa **Sulje**.
1. Valitse toimintoruudussa ensin **Tallenna** ja sitten **Tuo**.

Seuraavassa esimerkkikuvassa on Commercen **Vie Teamsin määritys** -ryhmä, jossa **Lisää yksikkö** -elementit ja viedyn CSV-tiedoston otsikot korostettuina.

![Commercen Vie Teamsin määritys -ryhmä, jossa Lisää yksikkö -elementit ja viedyn CSV-tiedoston otsikot korostettuina.](media/d365-commerce-data-mgmt-export-entity.png)

> [!NOTE]
> Kun olet suorittanut edelliset vaiheet, synkronoi tehtävänhallinta noudattamalla ohjetta [Synkronoi tehtävänhallinta Microsoft Teamsin ja myyntipisteen välillä](synchronize-tasks-teams-pos.md). 

## <a name="additional-resources"></a>Lisäresurssit

[Dynamics 365 Commercen ja Microsoft Teamsin integroinnin yleiskatsaus](commerce-teams-integration.md)

[Ota Dynamics 365 Commercen ja Microsoft Teamsin integraatio käyttöön](enable-teams-integration.md)

[Microsoft Teamsin valmistelu Dynamics 365 Commercesta](provision-teams-from-commerce.md)

[Tehtävien hallinnan synkronointi Microsoft Teamsin ja Dynamics 365 Commerce -myyntipisteen välillä](synchronize-tasks-teams-pos.md)

[Käyttäjäroolien hallinta Microsoft Teamsissa](manage-user-roles-teams.md)

[Dynamics 365 Commercen ja Microsoft Teamsin integrointi – usein kysytyt kysymykset](teams-integration-faq.md)
